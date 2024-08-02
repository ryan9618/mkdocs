# Rust版行事历
### tages:
    - Rust
    - 开发
    - Develop
    - Rust版行事历
    - 
```
use std::collections::HashMap;

struct CalendarEntry {
    id: usize,
    matter: String,
    content: String,
    importance: u8,
}

fn main() {
    // 存储日期到行事历项向量的映射
    let mut calendar: HashMap<String, Vec<CalendarEntry>> = HashMap::new();

    // 添加行事历项
    let date = "2023-09-05";
    let entries = calendar.entry(date.to_string()).or_insert_with(Vec::new);
    entries.push(CalendarEntry {
        id: 1,
        matter: "Meeting with client".to_string(),
        content: "Discuss project details".to_string(),
        importance: 3,
    });
    entries.push(CalendarEntry {
        id: 2,
        matter: "Lunch with friends".to_string(),
        content: "Order pizza".to_string(),
        importance: 2,
    });
    entries.push(CalendarEntry {
        id: 3,
        matter: "Gym workout".to_string(),
        content: "Go for a run".to_string(),
        importance: 1,
    });

    // 显示所有行事历
    for (date, entries) in &calendar {
        println!("Date: {}", date);
        for entry in entries {
            println!("ID: {}", entry.id);
            println!("Matter: {}", entry.matter);
            println!("Content: {}", entry.content);
            println!("Importance: {}", entry.importance);
        }
    }
}




//行事历改进版
use std::collections::HashMap;

struct CalendarEntry {
    id: usize,
    date: String,
    matter: String,
    content: String,
    importance: u8,
}

fn main() {
    // 存储序列号到行事历项的映射
    let mut calendar: HashMap<String, CalendarEntry> = HashMap::new(); // 哈希映射

    // 添加行事历项
    calendar.insert("T0001".to_string(), CalendarEntry {
        id: 1,
        date: "2023-09-05".to_string(),
        matter: "Meeting with client".to_string(),
        content: "Discuss project details".to_string(),
        importance: 3,
    });
    calendar.insert("T0002".to_string(), CalendarEntry {
        id: 2,
        date: "2023-09-05".to_string(),
        matter: "Lunch with friends".to_string(),
        content: "Order pizza".to_string(),
        importance: 2,
    });
    calendar.insert("T0003".to_string(), CalendarEntry {
        id: 3,
        date: "2023-09-05".to_string(),
        matter: "Gym workout".to_string(),
        content: "Go for a run".to_string(),
        importance: 1,
    });

    // 显示所有行事历
    for (serial_number, entry) in &calendar { // 遍历哈希映射中的键值对
        println!("Serial Number: {}", serial_number);
        println!("ID: {}", entry.id);
        println!("Date: {}", entry.date);
        println!("Matter: {}", entry.matter);
        println!("Content: {}", entry.content);
        println!("Importance: {}", entry.importance);
    }
}


//或则

use std::collections::HashMap;

struct CalendarEntry {
    id: usize,
    date: String,
    matter: String,
    content: String,
    importance: u8,
}

fn main() {
    // 存储序列号到行事历项的映射
    let mut calendar: HashMap<String, CalendarEntry> = HashMap::new(); // 哈希映射

    // 添加行事历项
    calendar.insert("T0001".to_string(), CalendarEntry {
        id: 1,
        date: "2023-09-05".to_string(),
        matter: "扫描".to_string(),
        content: "三天以后到云浮扫描石材".to_string(),
        importance: 3,
    });
    calendar.insert("T0002".to_string(), CalendarEntry {
        id: 2,
        date: "2023-09-05".to_string(),
        matter: "设计".to_string(),
        content: "做设计彩图".to_string(),
        importance: 2,
    });
    calendar.insert("T0003".to_string(), CalendarEntry {
        id: 3,
        date: "2023-09-05".to_string(),
        matter: "出差".to_string(),
        content: "具体不切的".to_string(),
        importance: 1,
    });
    println!("ID   Serial Numbe   日期        事项      内容      等级");
    // 显示所有行事历
    for (serial_number, entry) in &calendar { // 遍历哈希映射中的键值对
        
         println!("{}    {}       {}   {}     {}  {}", entry.id , serial_number, entry.date, entry.matter, entry.content, entry.importance);
        
        
       // println!("Serial Number: {}", serial_number);
       // println!("ID: {}", entry.id);
        //println!("日期: {}", entry.date);
       // println!("事项: {}", entry.matter);
        //println!("内容: {}", entry.content);
        //println!("等级: {}", entry.importance);
    }
}


```
   
