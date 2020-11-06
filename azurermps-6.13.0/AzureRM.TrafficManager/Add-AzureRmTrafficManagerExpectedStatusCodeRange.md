---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 32a00a6dce3d6a370f7b7f79f05794a312277a09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572566"
---
# <span data-ttu-id="ea447-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="ea447-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="ea447-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea447-102">SYNOPSIS</span></span>
<span data-ttu-id="ea447-103">Yerel bir Traffic Manager profil nesnesine beklenen bir durum kodu aralığı ekler.</span><span class="sxs-lookup"><span data-stu-id="ea447-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea447-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea447-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea447-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea447-105">DESCRIPTION</span></span>
<span data-ttu-id="ea447-106">**Add-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet 'i yerel bir Azure Traffic Manager profil nesnesine bir dizi beklenen durum kodu ekler.</span><span class="sxs-lookup"><span data-stu-id="ea447-106">The **Add-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="ea447-107">New-AzureRmTrafficManagerProfile veya Get-AzureRmTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea447-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="ea447-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="ea447-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="ea447-109">Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="ea447-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="ea447-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea447-110">EXAMPLES</span></span>

### <span data-ttu-id="ea447-111">Örnek 1: profile beklenen bir durum kodu aralığı ekleme</span><span class="sxs-lookup"><span data-stu-id="ea447-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="ea447-112">İlk komut **Get-AzureRmTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="ea447-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="ea447-113">Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.</span><span class="sxs-lookup"><span data-stu-id="ea447-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="ea447-114">İkinci komut, $TrafficManagerProfile depolanan profile beklenen bir durum kodu aralığı ekler.</span><span class="sxs-lookup"><span data-stu-id="ea447-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="ea447-115">Son komutu, Traffic Manager 'daki profili $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ea447-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="ea447-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea447-116">PARAMETERS</span></span>

### <span data-ttu-id="ea447-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea447-117">-DefaultProfile</span></span>
<span data-ttu-id="ea447-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea447-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea447-119">-Max</span><span class="sxs-lookup"><span data-stu-id="ea447-119">-Max</span></span>
<span data-ttu-id="ea447-120">Eklenecek durum kodu aralığındaki en yüksek değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea447-120">Specifies the highest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea447-121">-Dk</span><span class="sxs-lookup"><span data-stu-id="ea447-121">-Min</span></span>
<span data-ttu-id="ea447-122">Eklenecek durum kodu aralığındaki en düşük değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea447-122">Specifies the lowest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea447-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea447-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="ea447-124">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea447-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ea447-125">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ea447-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ea447-126">**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea447-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="ea447-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea447-127">-Confirm</span></span>
<span data-ttu-id="ea447-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea447-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea447-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea447-129">-WhatIf</span></span>
<span data-ttu-id="ea447-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea447-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea447-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea447-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea447-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea447-132">CommonParameters</span></span>
<span data-ttu-id="ea447-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea447-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea447-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea447-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea447-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea447-135">INPUTS</span></span>

### <span data-ttu-id="ea447-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea447-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="ea447-137">Bu cmdlet, bu cmdlet 'e bir **TrafficManagerProfile** nesnesi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="ea447-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="ea447-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea447-138">OUTPUTS</span></span>

### <span data-ttu-id="ea447-139">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea447-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="ea447-140">Bu cmdlet değiştirilmiş bir **TrafficManagerProfile** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="ea447-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="ea447-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea447-141">NOTES</span></span>

## <span data-ttu-id="ea447-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea447-142">RELATED LINKS</span></span>

[<span data-ttu-id="ea447-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="ea447-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="ea447-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea447-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ea447-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea447-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
