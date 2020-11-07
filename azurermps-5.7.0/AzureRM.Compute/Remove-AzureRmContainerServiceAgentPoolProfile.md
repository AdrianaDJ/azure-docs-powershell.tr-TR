---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: cfcb3c7657bc0ff99646c3ef21eb5cceb592fe2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762165"
---
# <span data-ttu-id="a0208-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="a0208-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="a0208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0208-102">SYNOPSIS</span></span>
<span data-ttu-id="a0208-103">Kapsayıcı hizmetten bir aracı havuzu profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0208-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0208-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0208-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [-Name] <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0208-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0208-105">DESCRIPTION</span></span>
<span data-ttu-id="a0208-106">**Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet 'i, bir kapsayıcı hizmetten bir aracı havuz profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0208-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="a0208-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0208-107">EXAMPLES</span></span>

### <span data-ttu-id="a0208-108">Örnek 1: kapsayıcı hizmetten profil kaldırma</span><span class="sxs-lookup"><span data-stu-id="a0208-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="a0208-109">İlk komut, Get-AzureRmContainerService cmdlet 'ini kullanarak CSResourceGroup17 adlı bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="a0208-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="a0208-110">Komut, hizmeti $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a0208-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="a0208-111">İkinci komut, $Container içinde kapsayıcı hizmetten AgentPool01 adlı profili kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0208-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="a0208-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0208-112">PARAMETERS</span></span>

### <span data-ttu-id="a0208-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="a0208-113">-ContainerService</span></span>
<span data-ttu-id="a0208-114">Bu cmdlet 'in bir aracı havuzu profilini kaldıran kapsayıcı hizmeti nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0208-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0208-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0208-115">-Name</span></span>
<span data-ttu-id="a0208-116">Bu cmdlet 'in kaldırdığı aracı havuz profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0208-116">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a0208-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0208-117">-Confirm</span></span>
<span data-ttu-id="a0208-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0208-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0208-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0208-119">-WhatIf</span></span>
<span data-ttu-id="a0208-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0208-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0208-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0208-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0208-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0208-122">CommonParameters</span></span>
<span data-ttu-id="a0208-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0208-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0208-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0208-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0208-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0208-125">INPUTS</span></span>

### <span data-ttu-id="a0208-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a0208-126">None</span></span>
<span data-ttu-id="a0208-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a0208-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0208-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0208-128">OUTPUTS</span></span>

## <span data-ttu-id="a0208-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0208-129">NOTES</span></span>

## <span data-ttu-id="a0208-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0208-130">RELATED LINKS</span></span>

[<span data-ttu-id="a0208-131">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="a0208-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="a0208-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a0208-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


