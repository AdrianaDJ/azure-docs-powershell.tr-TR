---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: c8ee3324f7f6e7653d86bef747bdb9831982474e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589085"
---
# <span data-ttu-id="08f58-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="08f58-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="08f58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08f58-102">SYNOPSIS</span></span>
<span data-ttu-id="08f58-103">Kümedeki birincil düğümün güvenilirlik katmanını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="08f58-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08f58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08f58-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08f58-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="08f58-105">DESCRIPTION</span></span>
<span data-ttu-id="08f58-106">Kümedeki birincil düğüm türünün güvenilirliğini güncelleştirmek için **Update-Azurermservicefabricgüvenilirliği** 'nı kullanın.</span><span class="sxs-lookup"><span data-stu-id="08f58-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="08f58-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08f58-107">EXAMPLES</span></span>

### <span data-ttu-id="08f58-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="08f58-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="08f58-109">Bu komut, birincil düğümün güvenilirlik katmanını gümüş olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="08f58-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="08f58-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08f58-110">PARAMETERS</span></span>

### <span data-ttu-id="08f58-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="08f58-111">-AutoAddNode</span></span>
<span data-ttu-id="08f58-112">Güvenilirliği değiştirirken düğüm sayısını otomatik olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="08f58-112">Add node count automatically when changing reliability.</span></span>

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

### <span data-ttu-id="08f58-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="08f58-113">-Name</span></span>
<span data-ttu-id="08f58-114">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="08f58-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="08f58-115">-Reliityitylevel</span><span class="sxs-lookup"><span data-stu-id="08f58-115">-ReliabilityLevel</span></span>
<span data-ttu-id="08f58-116">Güvenilirlik katmanı.</span><span class="sxs-lookup"><span data-stu-id="08f58-116">Reliability tier.</span></span>

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

### <span data-ttu-id="08f58-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f58-117">-ResourceGroupName</span></span>
<span data-ttu-id="08f58-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="08f58-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="08f58-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="08f58-119">-Confirm</span></span>
<span data-ttu-id="08f58-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08f58-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f58-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f58-121">-WhatIf</span></span>
<span data-ttu-id="08f58-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08f58-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08f58-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08f58-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f58-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f58-124">-DefaultProfile</span></span>
<span data-ttu-id="08f58-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08f58-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08f58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f58-126">CommonParameters</span></span>
<span data-ttu-id="08f58-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08f58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f58-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08f58-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f58-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08f58-129">INPUTS</span></span>

### <span data-ttu-id="08f58-130">Microsoft. Azure. Commands. ServiceFabric. modeller. Reliityitylevel</span><span class="sxs-lookup"><span data-stu-id="08f58-130">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="08f58-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="08f58-131">System.Management.Automation.SwitchParameter</span></span>

<span data-ttu-id="08f58-132">System. String</span><span class="sxs-lookup"><span data-stu-id="08f58-132">System.String</span></span>

## <span data-ttu-id="08f58-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08f58-133">OUTPUTS</span></span>

### <span data-ttu-id="08f58-134">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="08f58-134">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="08f58-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08f58-135">NOTES</span></span>

## <span data-ttu-id="08f58-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08f58-136">RELATED LINKS</span></span>

