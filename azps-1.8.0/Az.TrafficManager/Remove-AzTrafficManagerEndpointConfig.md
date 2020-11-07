---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: f40587460cf5e4a1d7f06bfb88229f6e4e3f7975
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753866"
---
# <span data-ttu-id="3fad8-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3fad8-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="3fad8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fad8-102">SYNOPSIS</span></span>
<span data-ttu-id="3fad8-103">Yerel Traffic Manager profil nesnesinden uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3fad8-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="3fad8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3fad8-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fad8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3fad8-105">DESCRIPTION</span></span>
<span data-ttu-id="3fad8-106">**Remove-AzTrafficManagerEndpointConfig** cmdlet 'ı yerel Azure Traffic Manager profil nesnesinden bir uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3fad8-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="3fad8-107">Get-AzTrafficManagerProfile cmdlet 'ini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3fad8-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="3fad8-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="3fad8-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="3fad8-109">Set-AzTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="3fad8-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="3fad8-110">Uç noktayı kaldırmak ve değişiklikleri tek bir işlemde uygulamak için Remove-AzTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3fad8-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="3fad8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3fad8-111">EXAMPLES</span></span>

### <span data-ttu-id="3fad8-112">Örnek 1: uç noktayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="3fad8-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="3fad8-113">İlk komut **Get-AzTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="3fad8-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="3fad8-114">Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.</span><span class="sxs-lookup"><span data-stu-id="3fad8-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="3fad8-115">İkinci komut $TrafficManagerProfile uygulamasında depolanan profilden contoso adlı bir Azure uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3fad8-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="3fad8-116">Bu komut yalnızca yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3fad8-116">This command changes only the local object.</span></span>

<span data-ttu-id="3fad8-117">Son komut, ContosoProfile adlı Traffic Manager profilini $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3fad8-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="3fad8-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3fad8-118">PARAMETERS</span></span>

### <span data-ttu-id="3fad8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fad8-119">-DefaultProfile</span></span>
<span data-ttu-id="3fad8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3fad8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fad8-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3fad8-121">-EndpointName</span></span>
<span data-ttu-id="3fad8-122">Bu cmdlet 'in kaldırdığı Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3fad8-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fad8-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3fad8-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="3fad8-124">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3fad8-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="3fad8-125">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3fad8-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="3fad8-126">**TrafficManagerProfile** nesnesi almak için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3fad8-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fad8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fad8-127">CommonParameters</span></span>
<span data-ttu-id="3fad8-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3fad8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fad8-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fad8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fad8-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3fad8-130">INPUTS</span></span>

### <span data-ttu-id="3fad8-131">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3fad8-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3fad8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3fad8-132">OUTPUTS</span></span>

### <span data-ttu-id="3fad8-133">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3fad8-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3fad8-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3fad8-134">NOTES</span></span>

## <span data-ttu-id="3fad8-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3fad8-135">RELATED LINKS</span></span>

[<span data-ttu-id="3fad8-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3fad8-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="3fad8-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3fad8-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="3fad8-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3fad8-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="3fad8-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3fad8-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


