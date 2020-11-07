---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: f7ac75789e4020d3d0e645e5dac8ef2430795eb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591262"
---
# <span data-ttu-id="c8d32-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c8d32-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="c8d32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8d32-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d32-103">Traffic Manager profili etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c8d32-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8d32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8d32-104">SYNTAX</span></span>

### <span data-ttu-id="c8d32-105">Alanlardır</span><span class="sxs-lookup"><span data-stu-id="c8d32-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8d32-106">Nesnelerini</span><span class="sxs-lookup"><span data-stu-id="c8d32-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8d32-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8d32-107">DESCRIPTION</span></span>
<span data-ttu-id="c8d32-108">**Enable-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili sağlar.</span><span class="sxs-lookup"><span data-stu-id="c8d32-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c8d32-109">Düzen nesnesini ardışık düzen veya parametre değeri olarak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8d32-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="c8d32-110">Alternatif olarak, *Name* ve *resourcegroupname* parametrelerini kullanarak profili belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8d32-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="c8d32-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8d32-111">EXAMPLES</span></span>

### <span data-ttu-id="c8d32-112">Örnek 1: adla belirtilen bir profili etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="c8d32-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c8d32-113">Bu komut, ResourceGroup11 'da ContosoProfile adlı profili etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="c8d32-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="c8d32-114">Örnek 2: ardışık düzeni kullanarak profili etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="c8d32-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="c8d32-115">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="c8d32-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c8d32-116">Komut daha sonra bu profili, ardışık düzen işlecini kullanarak **Enable-AzureRmTrafficManagerProfile** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="c8d32-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c8d32-117">Bu cmdlet bu profili etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="c8d32-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="c8d32-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8d32-118">PARAMETERS</span></span>

### <span data-ttu-id="c8d32-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d32-119">-DefaultProfile</span></span>
<span data-ttu-id="c8d32-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8d32-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8d32-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c8d32-121">-Name</span></span>
<span data-ttu-id="c8d32-122">Bu cmdlet 'in etkinleştirmesine sahip olan Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8d32-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="c8d32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d32-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8d32-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8d32-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c8d32-125">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager profili etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c8d32-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c8d32-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c8d32-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="c8d32-127">Etkinleştirilecek bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8d32-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="c8d32-128">**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c8d32-128">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="c8d32-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d32-129">CommonParameters</span></span>
<span data-ttu-id="c8d32-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8d32-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d32-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d32-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d32-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8d32-132">INPUTS</span></span>

### <span data-ttu-id="c8d32-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c8d32-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="c8d32-134">Bu cmdlet bir **TrafficManagerProfile** nesnesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="c8d32-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="c8d32-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8d32-135">OUTPUTS</span></span>

### <span data-ttu-id="c8d32-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8d32-136">System.Boolean</span></span>

## <span data-ttu-id="c8d32-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8d32-137">NOTES</span></span>

## <span data-ttu-id="c8d32-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8d32-138">RELATED LINKS</span></span>

[<span data-ttu-id="c8d32-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c8d32-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c8d32-140">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c8d32-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c8d32-141">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c8d32-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c8d32-142">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c8d32-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c8d32-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c8d32-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

