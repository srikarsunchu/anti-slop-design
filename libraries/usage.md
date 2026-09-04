# Trusted libraries

Do not hand-roll these. Each is either headless or gorgeous by default, does
one thing completely including the invisible edge cases, treats accessibility
as load-bearing, and adopts in one line.

| Problem | Package | Install |
|---|---|---|
| animated numbers | `@number-flow/react` | `npm i @number-flow/react` |
| ⌘K command menu | `cmdk` | `npm i cmdk` |
| toasts | `sonner` | `npm i sonner` |
| OTP / 2FA | `input-otp` | `npm i input-otp` |
| live tuning panel | `leva` | `npm i leva` |
| long lists | `react-virtuoso` | `npm i react-virtuoso` |
| drag and drop | `@dnd-kit/core @dnd-kit/sortable @dnd-kit/utilities` | `npm i` those |
| streaming chart | `liveline` | `npm i liveline` |

Check versions before trusting a snippet: `npm view <pkg> version`. Read the
package's own README in node_modules if an API looks different.

## NumberFlow

```tsx
import NumberFlow from '@number-flow/react'
<NumberFlow value={value} format={{ style: 'currency', currency: 'USD' }} />
```

Respects reduced motion by default. `NumberFlowGroup` syncs several.

## cmdk

```tsx
import { Command } from 'cmdk'
<Command.Dialog open={open} onOpenChange={setOpen} label="Command menu">
  <Command.Input placeholder="Type a command" />
  <Command.List>
    <Command.Empty>No results.</Command.Empty>
    <Command.Group heading="Scenes">
      <Command.Item onSelect={() => go('14')}>Scene 14 · Diner</Command.Item>
    </Command.Group>
  </Command.List>
</Command.Dialog>
```

Unstyled. Style via `[cmdk-root]`, `[cmdk-item]` attributes. Each item needs
a unique value.

## Sonner

```tsx
import { Toaster, toast } from 'sonner'
<Toaster position="bottom-right" />
toast.success('Saved')
toast('Moved 15C to Day 4', { action: { label: 'Undo', onClick: undo } })
toast.promise(save(), { loading: 'Saving', success: 'Saved', error: 'Failed' })
```

## input-otp

```tsx
import { OTPInput } from 'input-otp'
<OTPInput maxLength={6} render={({ slots }) => (
  <div className="flex gap-2">{slots.map((s, i) => <Slot key={i} {...s} />)}</div>
)} />
```

One hidden input rendered as slots, so paste, SMS autofill, and screen readers
all work.

## Leva

```tsx
import { useControls } from 'leva'
const { speed } = useControls({ speed: { value: 1, min: 0, max: 5, step: .1 } })
```

## Virtuoso

```tsx
import { Virtuoso } from 'react-virtuoso'
<Virtuoso data={shots} itemContent={(i, shot) => <Row {...shot} />} style={{ height: 480 }} />
```

Variable heights without measuring. `endReached` for infinite scroll.

## dnd-kit

```tsx
import { DndContext, closestCenter } from '@dnd-kit/core'
import { SortableContext, useSortable, verticalListSortingStrategy } from '@dnd-kit/sortable'
import { CSS } from '@dnd-kit/utilities'
function Item({ id }) {
  const { attributes, listeners, setNodeRef, transform, transition } = useSortable({ id })
  return <div ref={setNodeRef} {...attributes} {...listeners}
    style={{ transform: CSS.Transform.toString(transform), transition }} />
}
<DndContext collisionDetection={closestCenter} onDragEnd={onDragEnd}>
  <SortableContext items={ids} strategy={verticalListSortingStrategy}>
    {ids.map(id => <Item key={id} id={id} />)}
  </SortableContext>
</DndContext>
```

Keyboard accessible out of the box.

## Liveline

```tsx
import { Liveline } from 'liveline'
<Liveline data={points} value={latest} />
```

Young package. Read its README before deep use.
