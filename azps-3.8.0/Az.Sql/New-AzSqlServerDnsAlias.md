---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 66f8c3acc178a922868177200e6d4f1f8f50931f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938417"
---
# <span data-ttu-id="322d6-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="322d6-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="322d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="322d6-102">SYNOPSIS</span></span>
<span data-ttu-id="322d6-103">Bu komut yeni bir Azure SQL Server DNS diğer adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="322d6-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="322d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="322d6-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="322d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="322d6-105">DESCRIPTION</span></span>
<span data-ttu-id="322d6-106">Belirtilen sunucunun üzerine gelerek yeni Azure SQL Server DNS diğer adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="322d6-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="322d6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="322d6-107">EXAMPLES</span></span>

### <span data-ttu-id="322d6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="322d6-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="322d6-109">Bu komut, sunucu serverName adına işaret eden ad adı olan Azure SQL Server DNS diğer adını oluşturur</span><span class="sxs-lookup"><span data-stu-id="322d6-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="322d6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="322d6-110">PARAMETERS</span></span>

### <span data-ttu-id="322d6-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="322d6-111">-AsJob</span></span>
<span data-ttu-id="322d6-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="322d6-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322d6-113">-DefaultProfile</span></span>
<span data-ttu-id="322d6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="322d6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="322d6-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="322d6-115">-Name</span></span>
<span data-ttu-id="322d6-116">Azure SQL Server DNS diğer adı.</span><span class="sxs-lookup"><span data-stu-id="322d6-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322d6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="322d6-117">-ResourceGroupName</span></span>
<span data-ttu-id="322d6-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="322d6-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="322d6-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="322d6-119">-ServerName</span></span>
<span data-ttu-id="322d6-120">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="322d6-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="322d6-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="322d6-121">-Confirm</span></span>
<span data-ttu-id="322d6-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="322d6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="322d6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="322d6-123">-WhatIf</span></span>
<span data-ttu-id="322d6-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="322d6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="322d6-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="322d6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="322d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322d6-126">CommonParameters</span></span>
<span data-ttu-id="322d6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="322d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322d6-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="322d6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322d6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="322d6-129">INPUTS</span></span>

### <span data-ttu-id="322d6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="322d6-130">System.String</span></span>

## <span data-ttu-id="322d6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="322d6-131">OUTPUTS</span></span>

### <span data-ttu-id="322d6-132">Microsoft. Azure. Commands. Sql. Serverdnsalıas. model. Azuressqlserverdnsaliasmodel</span><span class="sxs-lookup"><span data-stu-id="322d6-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="322d6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="322d6-133">NOTES</span></span>

## <span data-ttu-id="322d6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="322d6-134">RELATED LINKS</span></span>
