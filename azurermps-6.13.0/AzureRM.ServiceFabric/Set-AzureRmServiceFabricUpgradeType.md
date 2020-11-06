---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: ddab39c3ad575cd46c427c7346fd635217c0dbca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590847"
---
# <span data-ttu-id="d8e09-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="d8e09-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="d8e09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e09-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e09-103">Kümenin hizmet yapısı yükseltme türünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d8e09-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8e09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8e09-104">SYNTAX</span></span>

### <span data-ttu-id="d8e09-105">Otomatik</span><span class="sxs-lookup"><span data-stu-id="d8e09-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8e09-106">El ile</span><span class="sxs-lookup"><span data-stu-id="d8e09-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e09-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8e09-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e09-108">Belirli bir hizmet yapısı kodu sürümüyle yükseltme türünü otomatik veya el ile ayarlamak için **set-AzureRmServiceFabricUpgradeType** kullanın.</span><span class="sxs-lookup"><span data-stu-id="d8e09-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="d8e09-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8e09-109">EXAMPLES</span></span>

### <span data-ttu-id="d8e09-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8e09-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="d8e09-111">Bu komut küme yükseltme modunu otomatik olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d8e09-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="d8e09-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8e09-112">PARAMETERS</span></span>

### <span data-ttu-id="d8e09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e09-113">-DefaultProfile</span></span>
<span data-ttu-id="d8e09-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8e09-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8e09-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8e09-115">-Name</span></span>
<span data-ttu-id="d8e09-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d8e09-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d8e09-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e09-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8e09-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8e09-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d8e09-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="d8e09-119">-UpgradeMode</span></span>
<span data-ttu-id="d8e09-120">Clusterupgrademodu</span><span class="sxs-lookup"><span data-stu-id="d8e09-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e09-121">-Version</span><span class="sxs-lookup"><span data-stu-id="d8e09-121">-Version</span></span>
<span data-ttu-id="d8e09-122">Küme kodu sürümü.</span><span class="sxs-lookup"><span data-stu-id="d8e09-122">Cluster code version.</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e09-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8e09-123">-Confirm</span></span>
<span data-ttu-id="d8e09-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8e09-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e09-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e09-125">-WhatIf</span></span>
<span data-ttu-id="d8e09-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8e09-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8e09-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8e09-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e09-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e09-128">CommonParameters</span></span>
<span data-ttu-id="d8e09-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8e09-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e09-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e09-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e09-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8e09-131">INPUTS</span></span>

### <span data-ttu-id="d8e09-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d8e09-132">System.String</span></span>
<span data-ttu-id="d8e09-133">Parametreler: Version (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d8e09-133">Parameters: Version (ByValue)</span></span>

### <span data-ttu-id="d8e09-134">Microsoft. Azure. Commands. ServiceFabric. modeller. Kümeupgrademode</span><span class="sxs-lookup"><span data-stu-id="d8e09-134">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="d8e09-135">Parametreler: yükseltme modu (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d8e09-135">Parameters: UpgradeMode (ByValue)</span></span>

## <span data-ttu-id="d8e09-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8e09-136">OUTPUTS</span></span>

### <span data-ttu-id="d8e09-137">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="d8e09-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d8e09-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8e09-138">NOTES</span></span>

## <span data-ttu-id="d8e09-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8e09-139">RELATED LINKS</span></span>
