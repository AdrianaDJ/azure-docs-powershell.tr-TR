---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268425"
---
# <span data-ttu-id="2d05d-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d05d-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="2d05d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d05d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d05d-103">Çalışma alanı için bağlantılı depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="2d05d-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="2d05d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d05d-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d05d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d05d-105">DESCRIPTION</span></span>
<span data-ttu-id="2d05d-106">Çalışma alanı için bağlantılı depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="2d05d-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="2d05d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d05d-107">EXAMPLES</span></span>

### <span data-ttu-id="2d05d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d05d-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="2d05d-109">Çalışma alanı için bağlantılı depolama alanı ayarlama</span><span class="sxs-lookup"><span data-stu-id="2d05d-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="2d05d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d05d-110">PARAMETERS</span></span>

### <span data-ttu-id="2d05d-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="2d05d-111">-DataSourceType</span></span>
<span data-ttu-id="2d05d-112">Veri kaynağı türü ' CustomLogs ', ' AzureWatson ' değerinden biri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2d05d-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d05d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d05d-113">-DefaultProfile</span></span>
<span data-ttu-id="2d05d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d05d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d05d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d05d-115">-Force</span></span>
<span data-ttu-id="2d05d-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="2d05d-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2d05d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d05d-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d05d-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2d05d-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d05d-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="2d05d-119">-StorageAccountIds</span></span>
<span data-ttu-id="2d05d-120">Depolama hesap kimliğinin listesi.</span><span class="sxs-lookup"><span data-stu-id="2d05d-120">list of storage account Id.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d05d-121">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="2d05d-121">-WorkspaceName</span></span>
<span data-ttu-id="2d05d-122">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="2d05d-122">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d05d-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d05d-123">-Confirm</span></span>
<span data-ttu-id="2d05d-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d05d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d05d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d05d-125">-WhatIf</span></span>
<span data-ttu-id="2d05d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d05d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d05d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d05d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d05d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d05d-128">CommonParameters</span></span>
<span data-ttu-id="2d05d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d05d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d05d-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2d05d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d05d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d05d-131">INPUTS</span></span>

### <span data-ttu-id="2d05d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2d05d-132">System.String</span></span>

## <span data-ttu-id="2d05d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d05d-133">OUTPUTS</span></span>

### <span data-ttu-id="2d05d-134">Microsoft. Azure. Commands. Operationalınsights. modeller. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="2d05d-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="2d05d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d05d-135">NOTES</span></span>

## <span data-ttu-id="2d05d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d05d-136">RELATED LINKS</span></span>
