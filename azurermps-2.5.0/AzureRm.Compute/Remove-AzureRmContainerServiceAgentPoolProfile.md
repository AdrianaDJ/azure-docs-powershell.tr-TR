---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939767"
---
# <span data-ttu-id="3eb5d-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="3eb5d-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="3eb5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb5d-103">Kapsayıcı hizmetten bir aracı havuzu profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eb5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3eb5d-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb5d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3eb5d-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb5d-106">**Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet 'i, bir kapsayıcı hizmetten bir aracı havuz profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="3eb5d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3eb5d-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb5d-108">Örnek 1: kapsayıcı hizmetten profil kaldırma</span><span class="sxs-lookup"><span data-stu-id="3eb5d-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="3eb5d-109">İlk komut, Get-AzureRmContainerService cmdlet 'ini kullanarak CSResourceGroup17 adlı bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="3eb5d-110">Komut, hizmeti $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="3eb5d-111">İkinci komut, $Container içinde kapsayıcı hizmetten AgentPool01 adlı profili kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="3eb5d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3eb5d-112">PARAMETERS</span></span>

### <span data-ttu-id="3eb5d-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="3eb5d-113">-ContainerService</span></span>
<span data-ttu-id="3eb5d-114">Bu cmdlet 'in bir aracı havuzu profilini kaldıran kapsayıcı hizmeti nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb5d-115">-DefaultProfile</span></span>
<span data-ttu-id="3eb5d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eb5d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3eb5d-117">-Name</span></span>
<span data-ttu-id="3eb5d-118">Bu cmdlet 'in kaldırdığı aracı havuz profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3eb5d-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3eb5d-119">-Confirm</span></span>
<span data-ttu-id="3eb5d-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb5d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb5d-121">-WhatIf</span></span>
<span data-ttu-id="3eb5d-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3eb5d-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb5d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb5d-124">CommonParameters</span></span>
<span data-ttu-id="3eb5d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3eb5d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb5d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb5d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb5d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3eb5d-127">INPUTS</span></span>

### <span data-ttu-id="3eb5d-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="3eb5d-128">ContainerService</span></span>
<span data-ttu-id="3eb5d-129">Parametre ' ContainerService ', ardışık düzenin ' ContainerService ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3eb5d-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="3eb5d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3eb5d-130">OUTPUTS</span></span>

### <span data-ttu-id="3eb5d-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="3eb5d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="3eb5d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3eb5d-132">NOTES</span></span>

## <span data-ttu-id="3eb5d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3eb5d-133">RELATED LINKS</span></span>

[<span data-ttu-id="3eb5d-134">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="3eb5d-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="3eb5d-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3eb5d-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


