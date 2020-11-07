---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 516fd126b1015bca23c34a4eb295a03752e836f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758940"
---
# <span data-ttu-id="b9c12-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="b9c12-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="b9c12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c12-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c12-103">Azure SQL Server DNS diğer adını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="b9c12-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="b9c12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9c12-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9c12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9c12-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c12-106">Tüm Azure SQL Server DNS diğer adlarını alın veya sunucunun tüm sunucu DNS diğer adlarını listeler</span><span class="sxs-lookup"><span data-stu-id="b9c12-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="b9c12-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9c12-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c12-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b9c12-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="b9c12-109">Belirli bir sunucunun tüm sunucu DNS diğer adlarını listeler</span><span class="sxs-lookup"><span data-stu-id="b9c12-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="b9c12-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b9c12-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="b9c12-111">Sunucu ve diğer ad tarafından belirtilen sunucu DNS diğer adını alır</span><span class="sxs-lookup"><span data-stu-id="b9c12-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="b9c12-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b9c12-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="b9c12-113">"Dnsaliasname" ile başlayan belirli sunucu DNS diğer adlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b9c12-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="b9c12-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9c12-114">PARAMETERS</span></span>

### <span data-ttu-id="b9c12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c12-115">-DefaultProfile</span></span>
<span data-ttu-id="b9c12-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9c12-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c12-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9c12-117">-Name</span></span>
<span data-ttu-id="b9c12-118">Azure SQL Server DNS diğer adı.</span><span class="sxs-lookup"><span data-stu-id="b9c12-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="b9c12-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c12-119">-ResourceGroupName</span></span>
<span data-ttu-id="b9c12-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b9c12-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c12-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9c12-121">-ServerName</span></span>
<span data-ttu-id="b9c12-122">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="b9c12-122">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c12-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="b9c12-123">-Confirm</span></span>
<span data-ttu-id="b9c12-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b9c12-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c12-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c12-125">-WhatIf</span></span>
<span data-ttu-id="b9c12-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b9c12-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c12-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b9c12-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c12-128">CommonParameters</span></span>
<span data-ttu-id="b9c12-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9c12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c12-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b9c12-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c12-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9c12-131">INPUTS</span></span>

### <span data-ttu-id="b9c12-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c12-132">System.String</span></span>

## <span data-ttu-id="b9c12-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9c12-133">OUTPUTS</span></span>

### <span data-ttu-id="b9c12-134">Microsoft. Azure. Commands. Sql. Serverdnsalıas. model. Azuressqlserverdnsaliasmodel</span><span class="sxs-lookup"><span data-stu-id="b9c12-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="b9c12-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9c12-135">NOTES</span></span>

## <span data-ttu-id="b9c12-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9c12-136">RELATED LINKS</span></span>
