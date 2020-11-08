---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279268"
---
# <span data-ttu-id="836eb-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="836eb-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="836eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="836eb-102">SYNOPSIS</span></span>
<span data-ttu-id="836eb-103">Traffic Manager profili etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="836eb-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="836eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="836eb-104">SYNTAX</span></span>

### <span data-ttu-id="836eb-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="836eb-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="836eb-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="836eb-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="836eb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="836eb-107">DESCRIPTION</span></span>
<span data-ttu-id="836eb-108">**Enable-AzTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili sağlar.</span><span class="sxs-lookup"><span data-stu-id="836eb-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="836eb-109">Düzen nesnesini ardışık düzen veya parametre değeri olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="836eb-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="836eb-110">Alternatif olarak, *Name* ve *resourcegroupname* parametrelerini kullanarak profili belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="836eb-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="836eb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="836eb-111">EXAMPLES</span></span>

### <span data-ttu-id="836eb-112">Örnek 1: adla belirtilen bir profili etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="836eb-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="836eb-113">Bu komut, ResourceGroup11 'da ContosoProfile adlı profili etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="836eb-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="836eb-114">Örnek 2: ardışık düzeni kullanarak profili etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="836eb-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="836eb-115">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="836eb-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="836eb-116">Komut daha sonra bu profili, ardışık düzen işlecini kullanarak **Enable-AzTrafficManagerProfile** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="836eb-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="836eb-117">Bu cmdlet bu profili etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="836eb-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="836eb-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="836eb-118">PARAMETERS</span></span>

### <span data-ttu-id="836eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="836eb-119">-DefaultProfile</span></span>
<span data-ttu-id="836eb-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="836eb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="836eb-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="836eb-121">-Name</span></span>
<span data-ttu-id="836eb-122">Bu cmdlet 'in etkinleştirmesine sahip olan Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="836eb-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836eb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="836eb-123">-ResourceGroupName</span></span>
<span data-ttu-id="836eb-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="836eb-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="836eb-125">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager profili etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="836eb-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="836eb-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="836eb-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="836eb-127">Etkinleştirilecek bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="836eb-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="836eb-128">**TrafficManagerProfile** nesnesi almak için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="836eb-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="836eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836eb-129">CommonParameters</span></span>
<span data-ttu-id="836eb-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="836eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836eb-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="836eb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836eb-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="836eb-132">INPUTS</span></span>

### <span data-ttu-id="836eb-133">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="836eb-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="836eb-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="836eb-134">OUTPUTS</span></span>

### <span data-ttu-id="836eb-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="836eb-135">System.Boolean</span></span>

## <span data-ttu-id="836eb-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="836eb-136">NOTES</span></span>

## <span data-ttu-id="836eb-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="836eb-137">RELATED LINKS</span></span>

[<span data-ttu-id="836eb-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="836eb-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="836eb-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="836eb-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="836eb-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="836eb-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="836eb-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="836eb-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="836eb-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="836eb-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


