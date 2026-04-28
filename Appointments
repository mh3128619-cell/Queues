from collections import deque

appointments = deque()
undo_stack = []

def add_appointment(name):
    appointments.append(name)
    print(f"✅ Appointment registered for: {name}")

def serve_customer():
    if appointments:
        current = appointments.popleft()
        undo_stack.append(current)
        print(f"🔔 Now serving: {current}")
    else:
        print("📭 The queue is empty!")

def undo_last_serve():
    if undo_stack:
        last_person = undo_stack.pop()
        appointments.appendleft(last_person)
        print(f"⏪ Undo: Moved {last_person} back to the front of the queue.")
    else:
        print("❌ No undo operations available.")

add_appointment("Ahmed")
add_appointment("Sara")
add_appointment("Ali")

print(f"Current Queue: {list(appointments)}")

serve_customer()
serve_customer()

print(f"Queue after serving: {list(appointments)}")

undo_last_serve()

print(f"Final Queue: {list(appointments)}")
