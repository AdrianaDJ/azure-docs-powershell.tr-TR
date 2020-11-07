---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938410"
---
# <span data-ttu-id="085ff-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="085ff-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="085ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="085ff-102">SYNOPSIS</span></span>
<span data-ttu-id="085ff-103">Azure SQL eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="085ff-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="085ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="085ff-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="085ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="085ff-105">DESCRIPTION</span></span>
<span data-ttu-id="085ff-106">**New-AzSqlSyncAgentKey** cmdlet 'ı Azure SQL eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="085ff-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="085ff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="085ff-107">EXAMPLES</span></span>

### <span data-ttu-id="085ff-108">Örnek 1: Azure SQL eşitleme Aracısı için eşitleme Aracısı anahtarı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="085ff-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="085ff-109">Bu komut, Azure SQL eşitleme Aracısı için eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="085ff-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="085ff-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="085ff-110">PARAMETERS</span></span>

### <span data-ttu-id="085ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="085ff-111">-DefaultProfile</span></span>
<span data-ttu-id="085ff-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="085ff-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="085ff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="085ff-113">-ResourceGroupName</span></span>
<span data-ttu-id="085ff-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="085ff-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="085ff-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="085ff-115">-ServerName</span></span>
<span data-ttu-id="085ff-116">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="085ff-116">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="085ff-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="085ff-117">-SyncAgentName</span></span>
<span data-ttu-id="085ff-118">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="085ff-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="085ff-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="085ff-119">-Confirm</span></span>
<span data-ttu-id="085ff-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="085ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="085ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="085ff-121">-WhatIf</span></span>
<span data-ttu-id="085ff-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="085ff-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="085ff-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="085ff-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="085ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="085ff-124">CommonParameters</span></span>
<span data-ttu-id="085ff-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="085ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="085ff-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="085ff-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="085ff-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="085ff-127">INPUTS</span></span>

### <span data-ttu-id="085ff-128">System. String</span><span class="sxs-lookup"><span data-stu-id="085ff-128">System.String</span></span>

## <span data-ttu-id="085ff-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="085ff-129">OUTPUTS</span></span>

### <span data-ttu-id="085ff-130">Microsoft. Azure. Commands. Sql. DataSync. model. azures, Syncagentkeymodel</span><span class="sxs-lookup"><span data-stu-id="085ff-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="085ff-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="085ff-131">NOTES</span></span>

## <span data-ttu-id="085ff-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="085ff-132">RELATED LINKS</span></span>
