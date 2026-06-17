# HTML Editor

Hard autosave version:
- Immediate synchronous save to localStorage on every commit/mutation.
- Emergency current backup key.
- 10 rotating backup slots.
- IndexedDB backup still used as secondary storage.
- Auto-restore reads localStorage first before loading starter page.
- More menu has Restore Backup Slots and Force Save Now.
