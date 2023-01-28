# Get-function-name

function functionName( func )
{
 // Match:
 // - ^ the beginning of the string
 // - function the word 'function'
 // - \s+ at least some white space
 // - ([\w\$]+) capture one or more valid JavaScript identifier characters
 // - \( followed by an opening brace
 //
 var result = /^function\s+([\w\$]+)\(/.exec( func.toString() )
 
 return result ? result[1] : ''
}
