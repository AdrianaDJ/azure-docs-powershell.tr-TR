---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278079"
---
# <span data-ttu-id="d8a20-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8a20-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="d8a20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8a20-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a20-103">Çalışma alanı için bağlantılı depolama hesabını silme</span><span class="sxs-lookup"><span data-stu-id="d8a20-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="d8a20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8a20-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8a20-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8a20-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a20-106">Çalışma alanı için bağlantılı depolama hesabını silme</span><span class="sxs-lookup"><span data-stu-id="d8a20-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="d8a20-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8a20-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a20-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8a20-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="d8a20-109">{Workspace-Name} için "CustomLogs" türündeki bağlı depolama hesabını silme</span><span class="sxs-lookup"><span data-stu-id="d8a20-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="d8a20-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8a20-110">PARAMETERS</span></span>

### <span data-ttu-id="d8a20-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="d8a20-111">-DataSourceType</span></span>
<span data-ttu-id="d8a20-112">Veri kaynağı türü ' CustomLogs ', ' AzureWatson ' değerinden biri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d8a20-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a20-113">-DefaultProfile</span></span>
<span data-ttu-id="d8a20-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8a20-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8a20-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d8a20-115">-Force</span></span>
<span data-ttu-id="d8a20-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="d8a20-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d8a20-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8a20-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8a20-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d8a20-118">The resource group name.</span></span>

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

### <span data-ttu-id="d8a20-119">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="d8a20-119">-WorkspaceName</span></span>
<span data-ttu-id="d8a20-120">Çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="d8a20-120">The workspace name.</span></span>

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

### <span data-ttu-id="d8a20-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8a20-121">-Confirm</span></span>
<span data-ttu-id="d8a20-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8a20-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8a20-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8a20-123">-WhatIf</span></span>
<span data-ttu-id="d8a20-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8a20-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8a20-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8a20-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8a20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a20-126">CommonParameters</span></span>
<span data-ttu-id="d8a20-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8a20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a20-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d8a20-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a20-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8a20-129">INPUTS</span></span>

### <span data-ttu-id="d8a20-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d8a20-130">System.String</span></span>

## <span data-ttu-id="d8a20-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8a20-131">OUTPUTS</span></span>

### <span data-ttu-id="d8a20-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8a20-132">System.Boolean</span></span>

## <span data-ttu-id="d8a20-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8a20-133">NOTES</span></span>

## <span data-ttu-id="d8a20-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8a20-134">RELATED LINKS</span></span>
