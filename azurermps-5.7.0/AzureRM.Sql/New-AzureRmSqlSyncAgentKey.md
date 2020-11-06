---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: c6a9c1df9fca93b932ebc65a11c6b126b133465b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591555"
---
# <span data-ttu-id="c00bf-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="c00bf-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="c00bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c00bf-102">SYNOPSIS</span></span>
<span data-ttu-id="c00bf-103">Azure SQL eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c00bf-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c00bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c00bf-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c00bf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c00bf-105">DESCRIPTION</span></span>
<span data-ttu-id="c00bf-106">**Yeni-AzureRmSqlSyncAgentKey** cmdlet 'ı Azure SQL eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c00bf-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="c00bf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c00bf-107">EXAMPLES</span></span>

### <span data-ttu-id="c00bf-108">Örnek 1: Azure SQL eşitleme Aracısı için eşitleme Aracısı anahtarı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c00bf-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="c00bf-109">Bu komut, Azure SQL eşitleme Aracısı için eşitleme Aracısı anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c00bf-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="c00bf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c00bf-110">PARAMETERS</span></span>

### <span data-ttu-id="c00bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c00bf-111">-DefaultProfile</span></span>
<span data-ttu-id="c00bf-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c00bf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c00bf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c00bf-113">-ResourceGroupName</span></span>
<span data-ttu-id="c00bf-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c00bf-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="c00bf-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c00bf-115">-ServerName</span></span>
<span data-ttu-id="c00bf-116">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="c00bf-116">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c00bf-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="c00bf-117">-SyncAgentName</span></span>
<span data-ttu-id="c00bf-118">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="c00bf-118">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c00bf-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="c00bf-119">-Confirm</span></span>
<span data-ttu-id="c00bf-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c00bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c00bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c00bf-121">-WhatIf</span></span>
<span data-ttu-id="c00bf-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c00bf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c00bf-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c00bf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c00bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c00bf-124">CommonParameters</span></span>
<span data-ttu-id="c00bf-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c00bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c00bf-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c00bf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c00bf-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c00bf-127">INPUTS</span></span>

### <span data-ttu-id="c00bf-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c00bf-128">None</span></span>
<span data-ttu-id="c00bf-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c00bf-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c00bf-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c00bf-130">OUTPUTS</span></span>

### <span data-ttu-id="c00bf-131">Microsoft. Azure. Commands. Sql. DataSync. model. azures, Syncagentkeymodel</span><span class="sxs-lookup"><span data-stu-id="c00bf-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="c00bf-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c00bf-132">NOTES</span></span>

## <span data-ttu-id="c00bf-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c00bf-133">RELATED LINKS</span></span>
