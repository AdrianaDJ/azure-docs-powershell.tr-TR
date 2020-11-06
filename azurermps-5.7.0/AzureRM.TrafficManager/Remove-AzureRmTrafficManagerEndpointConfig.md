---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 7944328c7cac37d88cf18d715cbb7a893eacc683
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589641"
---
# <span data-ttu-id="2ca93-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2ca93-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="2ca93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ca93-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca93-103">Yerel Traffic Manager profil nesnesinden uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ca93-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ca93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ca93-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ca93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ca93-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca93-106">**Remove-AzureRmTrafficManagerEndpointConfig** cmdlet 'ı yerel Azure Traffic Manager profil nesnesinden bir uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ca93-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="2ca93-107">Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ca93-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="2ca93-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="2ca93-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="2ca93-109">Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2ca93-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="2ca93-110">Uç noktayı kaldırmak ve değişiklikleri tek bir işlemde uygulamak için Remove-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ca93-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="2ca93-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ca93-111">EXAMPLES</span></span>

### <span data-ttu-id="2ca93-112">Örnek 1: uç noktayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="2ca93-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="2ca93-113">İlk komut **Get-AzureRmTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="2ca93-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="2ca93-114">Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.</span><span class="sxs-lookup"><span data-stu-id="2ca93-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="2ca93-115">İkinci komut $TrafficManagerProfile uygulamasında depolanan profilden contoso adlı bir Azure uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ca93-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="2ca93-116">Bu komut yalnızca yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2ca93-116">This command changes only the local object.</span></span>

<span data-ttu-id="2ca93-117">Son komut, ContosoProfile adlı Traffic Manager profilini $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2ca93-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="2ca93-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ca93-118">PARAMETERS</span></span>

### <span data-ttu-id="2ca93-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca93-119">-DefaultProfile</span></span>
<span data-ttu-id="2ca93-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ca93-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ca93-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2ca93-121">-EndpointName</span></span>
<span data-ttu-id="2ca93-122">Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ca93-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca93-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ca93-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="2ca93-124">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ca93-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2ca93-125">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2ca93-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="2ca93-126">**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ca93-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca93-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca93-127">CommonParameters</span></span>
<span data-ttu-id="2ca93-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ca93-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca93-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca93-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca93-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ca93-130">INPUTS</span></span>

### <span data-ttu-id="2ca93-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ca93-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2ca93-132">Bu cmdlet, bu cmdlet 'e bir **TrafficManagerProfile** nesnesi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="2ca93-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="2ca93-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ca93-133">OUTPUTS</span></span>

### <span data-ttu-id="2ca93-134">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ca93-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2ca93-135">Bu cmdlet değiştirilmiş bir TrafficManagerProfile nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="2ca93-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="2ca93-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ca93-136">NOTES</span></span>

## <span data-ttu-id="2ca93-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ca93-137">RELATED LINKS</span></span>

[<span data-ttu-id="2ca93-138">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2ca93-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="2ca93-139">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ca93-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2ca93-140">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ca93-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2ca93-141">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ca93-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


