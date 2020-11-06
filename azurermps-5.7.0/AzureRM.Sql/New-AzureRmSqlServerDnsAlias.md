---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 897911a4f13b2453d0e814828000309ad8865ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591562"
---
# <span data-ttu-id="548a9-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="548a9-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="548a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="548a9-102">SYNOPSIS</span></span>
<span data-ttu-id="548a9-103">Bu komut yeni bir Azure SQL Server DNS diğer adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="548a9-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="548a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="548a9-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="548a9-105">DESCRIPTION</span></span>
<span data-ttu-id="548a9-106">Belirtilen sunucunun üzerine gelerek yeni Azure SQL Server DNS diğer adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="548a9-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="548a9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="548a9-107">EXAMPLES</span></span>

### <span data-ttu-id="548a9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="548a9-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="548a9-109">Bu komut, sunucu serverName adına işaret eden ad adı olan Azure SQL Server DNS diğer adını oluşturur</span><span class="sxs-lookup"><span data-stu-id="548a9-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="548a9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="548a9-110">PARAMETERS</span></span>

### <span data-ttu-id="548a9-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="548a9-111">-AsJob</span></span>
<span data-ttu-id="548a9-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="548a9-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548a9-113">-DefaultProfile</span></span>
<span data-ttu-id="548a9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="548a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548a9-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="548a9-115">-Name</span></span>
<span data-ttu-id="548a9-116">Azure SQL Server DNS diğer adı.</span><span class="sxs-lookup"><span data-stu-id="548a9-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548a9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548a9-117">-ResourceGroupName</span></span>
<span data-ttu-id="548a9-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="548a9-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548a9-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="548a9-119">-ServerName</span></span>
<span data-ttu-id="548a9-120">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="548a9-120">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548a9-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="548a9-121">-Confirm</span></span>
<span data-ttu-id="548a9-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="548a9-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548a9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548a9-123">-WhatIf</span></span>
<span data-ttu-id="548a9-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="548a9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548a9-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="548a9-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548a9-126">CommonParameters</span></span>
<span data-ttu-id="548a9-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="548a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548a9-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548a9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548a9-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="548a9-129">INPUTS</span></span>

### <span data-ttu-id="548a9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="548a9-130">System.String</span></span>

## <span data-ttu-id="548a9-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="548a9-131">OUTPUTS</span></span>

### <span data-ttu-id="548a9-132">Microsoft. Azure. Commands. Sql. Serverdnsalıas. model. Azuressqlserverdnsaliasmodel</span><span class="sxs-lookup"><span data-stu-id="548a9-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="548a9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="548a9-133">NOTES</span></span>

## <span data-ttu-id="548a9-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="548a9-134">RELATED LINKS</span></span>
