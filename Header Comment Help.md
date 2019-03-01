To open up a snippet file for editing, select ***User Snippets*** under `File` > `Preferences` and select the `create a new global snippet (New Global Snippets file)`.　　
## Then, Replace the following code　　
``` 
    {
	// Place your global snippets here. Each snippet is defined under a snippet name and has a scope, prefix, body and 
	// description. Add comma separated ids of the languages where the snippet is applicable in the scope field. If scope 
	// is left empty or omitted, the snippet gets applied to all languages. The prefix is what is 
	// used to trigger the snippet and the body will be expanded and inserted. Possible variables are: 
	// $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders. 
	// Placeholders with the same ids are connected.
	// Example:
	 "Headers comment": {
	 	"prefix": "My header_comment",
	 	"body": [
			
			"$BLOCK_COMMENT_START****************************************************************************************",
			//块注释开始，根据不同语言自动微调
			" ** FileName:        $TM_FILENAME",					
			//文件名称

			" ** Author:          Jiawei Hawkins", 		
			//作者名称（可修改） 

			" ** Date:            $CURRENT_YEAR-$CURRENT_MONTH-$CURRENT_DATE $CURRENT_DAY_NAME $CURRENT_HOUR:$CURRENT_MINUTE:$CURRENT_SECOND", 
			//具体日期时间（不可修改） 年-月-日 星期 时:分:秒

			" ** Description:     本次作业由本人独立实现完成，如有抄袭行为，愿承担由此带来的一切不良后果。", 
			//可加的细节描述
			" ****************************************************************************************$BLOCK_COMMENT_END",
			"",
			//块注释结束，根据不同语言自动微调
			"${0}",
	 	],
	 	"description": "Headers Comment"
	 }
}
``` 
## Then, every time you want to write a head-comment, just code `head`, that is enough
