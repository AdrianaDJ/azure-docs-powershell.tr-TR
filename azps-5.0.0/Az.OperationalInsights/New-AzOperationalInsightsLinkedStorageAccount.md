---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278081"
---
# <span data-ttu-id="03ec3-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="03ec3-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="03ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="03ec3-103">Çalışma alanı için bağlantılı depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="03ec3-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="03ec3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03ec3-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03ec3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="03ec3-106">Çalışma alanı için bağlantılı depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="03ec3-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="03ec3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03ec3-107">EXAMPLES</span></span>

### <span data-ttu-id="03ec3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="03ec3-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="03ec3-109">Çalışma alanı için bağlantılı depolama alanı ekleme</span><span class="sxs-lookup"><span data-stu-id="03ec3-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="03ec3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03ec3-110">PARAMETERS</span></span>

### <span data-ttu-id="03ec3-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="03ec3-111">-DataSourceType</span></span>
<span data-ttu-id="03ec3-112">Veri kaynağı türü ' CustomLogs ', ' AzureWatson ' değerinden biri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="03ec3-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="03ec3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ec3-113">-DefaultProfile</span></span>
<span data-ttu-id="03ec3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03ec3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03ec3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03ec3-115">-Force</span></span>
<span data-ttu-id="03ec3-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="03ec3-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="03ec3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ec3-117">-ResourceGroupName</span></span>
<span data-ttu-id="03ec3-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="03ec3-118">The resource group name.</span></span>

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

### <span data-ttu-id="03ec3-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="03ec3-119">-StorageAccountIds</span></span>
<span data-ttu-id="03ec3-120">Depolama hesap kimliğinin listesi.</span><span class="sxs-lookup"><span data-stu-id="03ec3-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="03ec3-121">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="03ec3-121">-WorkspaceName</span></span>
<span data-ttu-id="03ec3-122">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="03ec3-122">The workspace name.</span></span>

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

### <span data-ttu-id="03ec3-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="03ec3-123">-Confirm</span></span>
<span data-ttu-id="03ec3-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03ec3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03ec3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ec3-125">-WhatIf</span></span>
<span data-ttu-id="03ec3-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03ec3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03ec3-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03ec3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03ec3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ec3-128">CommonParameters</span></span>
<span data-ttu-id="03ec3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03ec3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ec3-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="03ec3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ec3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03ec3-131">INPUTS</span></span>

### <span data-ttu-id="03ec3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="03ec3-132">System.String</span></span>

## <span data-ttu-id="03ec3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03ec3-133">OUTPUTS</span></span>

### <span data-ttu-id="03ec3-134">Microsoft. Azure. Commands. Operationalınsights. modeller. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="03ec3-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="03ec3-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03ec3-135">NOTES</span></span>

## <span data-ttu-id="03ec3-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03ec3-136">RELATED LINKS</span></span>
