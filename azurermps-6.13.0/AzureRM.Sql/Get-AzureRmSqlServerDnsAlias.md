---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: cc85bea2739c379e960ffee29250bdc172e36765
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590004"
---
# <span data-ttu-id="8207a-101">Get-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="8207a-101">Get-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="8207a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8207a-102">SYNOPSIS</span></span>
<span data-ttu-id="8207a-103">Azure SQL Server DNS diğer adını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="8207a-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8207a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8207a-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8207a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8207a-105">DESCRIPTION</span></span>
<span data-ttu-id="8207a-106">Tüm Azure SQL Server DNS diğer adlarını alın veya sunucunun tüm sunucu DNS diğer adlarını listeler</span><span class="sxs-lookup"><span data-stu-id="8207a-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="8207a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8207a-107">EXAMPLES</span></span>

### <span data-ttu-id="8207a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8207a-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="8207a-109">Belirli bir sunucunun tüm sunucu DNS diğer adlarını listeler</span><span class="sxs-lookup"><span data-stu-id="8207a-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="8207a-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8207a-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="8207a-111">Sunucu ve diğer ad tarafından belirtilen sunucu DNS diğer adını alır</span><span class="sxs-lookup"><span data-stu-id="8207a-111">Gets Server DNS Alias specified by server and alias name</span></span>

## <span data-ttu-id="8207a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8207a-112">PARAMETERS</span></span>

### <span data-ttu-id="8207a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8207a-113">-DefaultProfile</span></span>
<span data-ttu-id="8207a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8207a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8207a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="8207a-115">-Name</span></span>
<span data-ttu-id="8207a-116">Azure SQL Server DNS diğer adı.</span><span class="sxs-lookup"><span data-stu-id="8207a-116">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8207a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8207a-117">-ResourceGroupName</span></span>
<span data-ttu-id="8207a-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8207a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="8207a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8207a-119">-ServerName</span></span>
<span data-ttu-id="8207a-120">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="8207a-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="8207a-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="8207a-121">-Confirm</span></span>
<span data-ttu-id="8207a-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8207a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8207a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8207a-123">-WhatIf</span></span>
<span data-ttu-id="8207a-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8207a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8207a-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8207a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8207a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8207a-126">CommonParameters</span></span>
<span data-ttu-id="8207a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8207a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8207a-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8207a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8207a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8207a-129">INPUTS</span></span>

### <span data-ttu-id="8207a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8207a-130">System.String</span></span>

## <span data-ttu-id="8207a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8207a-131">OUTPUTS</span></span>

### <span data-ttu-id="8207a-132">Microsoft. Azure. Commands. Sql. Serverdnsalıas. model. Azuressqlserverdnsaliasmodel</span><span class="sxs-lookup"><span data-stu-id="8207a-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="8207a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8207a-133">NOTES</span></span>

## <span data-ttu-id="8207a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8207a-134">RELATED LINKS</span></span>
