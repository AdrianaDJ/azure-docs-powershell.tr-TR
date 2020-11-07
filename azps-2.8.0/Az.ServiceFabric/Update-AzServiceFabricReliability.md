---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: 343c5c1a35334a25643aea576a9c545d1349e1f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933176"
---
# <span data-ttu-id="6ef98-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="6ef98-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="6ef98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ef98-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef98-103">Kümedeki birincil düğümün güvenilirlik katmanını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6ef98-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="6ef98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ef98-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ef98-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ef98-105">DESCRIPTION</span></span>
<span data-ttu-id="6ef98-106">Kümedeki birincil düğüm türünün güvenilirliğini güncelleştirmek için **Update-Azservicefabricgüvenirlik** kullanın.</span><span class="sxs-lookup"><span data-stu-id="6ef98-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="6ef98-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ef98-107">EXAMPLES</span></span>

### <span data-ttu-id="6ef98-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ef98-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="6ef98-109">Bu komut, birincil düğümün güvenilirlik katmanını gümüş olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6ef98-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="6ef98-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ef98-110">PARAMETERS</span></span>

### <span data-ttu-id="6ef98-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="6ef98-111">-AutoAddNode</span></span>
<span data-ttu-id="6ef98-112">Güvenilirliği değiştirirken düğüm sayısını otomatik olarak ekleme</span><span class="sxs-lookup"><span data-stu-id="6ef98-112">Add node count automatically when changing reliability</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ef98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef98-113">-DefaultProfile</span></span>
<span data-ttu-id="6ef98-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ef98-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ef98-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ef98-115">-Name</span></span>
<span data-ttu-id="6ef98-116">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="6ef98-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ef98-117">-Reliityitylevel</span><span class="sxs-lookup"><span data-stu-id="6ef98-117">-ReliabilityLevel</span></span>
<span data-ttu-id="6ef98-118">Güvenilirlik katmanı</span><span class="sxs-lookup"><span data-stu-id="6ef98-118">Reliability tier</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ef98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ef98-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ef98-120">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="6ef98-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6ef98-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ef98-121">-Confirm</span></span>
<span data-ttu-id="6ef98-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ef98-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ef98-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ef98-123">-WhatIf</span></span>
<span data-ttu-id="6ef98-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ef98-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ef98-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ef98-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ef98-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef98-126">CommonParameters</span></span>
<span data-ttu-id="6ef98-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ef98-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef98-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ef98-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef98-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ef98-129">INPUTS</span></span>

### <span data-ttu-id="6ef98-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6ef98-130">System.String</span></span>

### <span data-ttu-id="6ef98-131">Microsoft. Azure. Commands. ServiceFabric. modeller. Reliityitylevel</span><span class="sxs-lookup"><span data-stu-id="6ef98-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="6ef98-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6ef98-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6ef98-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ef98-133">OUTPUTS</span></span>

### <span data-ttu-id="6ef98-134">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="6ef98-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6ef98-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ef98-135">NOTES</span></span>

## <span data-ttu-id="6ef98-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ef98-136">RELATED LINKS</span></span>
