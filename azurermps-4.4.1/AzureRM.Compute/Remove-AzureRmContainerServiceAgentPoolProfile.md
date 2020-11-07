---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 355938c64926d0c97d7e1393abd5c8a0d5ce20ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594298"
---
# <span data-ttu-id="81724-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="81724-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="81724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81724-102">SYNOPSIS</span></span>
<span data-ttu-id="81724-103">Kapsayıcı hizmetten bir aracı havuzu profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81724-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81724-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81724-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81724-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81724-105">DESCRIPTION</span></span>
<span data-ttu-id="81724-106">**Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet 'i, bir kapsayıcı hizmetten bir aracı havuz profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81724-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="81724-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81724-107">EXAMPLES</span></span>

### <span data-ttu-id="81724-108">Örnek 1: kapsayıcı hizmetten profil kaldırma</span><span class="sxs-lookup"><span data-stu-id="81724-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="81724-109">İlk komut, Get-AzureRmContainerService cmdlet 'ini kullanarak CSResourceGroup17 adlı bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="81724-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="81724-110">Komut, hizmeti $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="81724-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="81724-111">İkinci komut, $Container içinde kapsayıcı hizmetten AgentPool01 adlı profili kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81724-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="81724-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81724-112">PARAMETERS</span></span>

### <span data-ttu-id="81724-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="81724-113">-ContainerService</span></span>
<span data-ttu-id="81724-114">Bu cmdlet 'in bir aracı havuzu profilini kaldıran kapsayıcı hizmeti nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81724-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81724-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81724-115">-DefaultProfile</span></span>
<span data-ttu-id="81724-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81724-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81724-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="81724-117">-Name</span></span>
<span data-ttu-id="81724-118">Bu cmdlet 'in kaldırdığı aracı havuz profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81724-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="81724-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="81724-119">-Confirm</span></span>
<span data-ttu-id="81724-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="81724-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81724-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81724-121">-WhatIf</span></span>
<span data-ttu-id="81724-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81724-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81724-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="81724-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81724-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81724-124">CommonParameters</span></span>
<span data-ttu-id="81724-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81724-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81724-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81724-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81724-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81724-127">INPUTS</span></span>

## <span data-ttu-id="81724-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81724-128">OUTPUTS</span></span>

## <span data-ttu-id="81724-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81724-129">NOTES</span></span>

## <span data-ttu-id="81724-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81724-130">RELATED LINKS</span></span>

[<span data-ttu-id="81724-131">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="81724-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="81724-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="81724-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

