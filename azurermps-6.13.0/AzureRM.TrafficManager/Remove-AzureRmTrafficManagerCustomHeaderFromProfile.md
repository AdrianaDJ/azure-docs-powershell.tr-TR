---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: af18a5a93cf08fe4806af429aee667b569c527d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764582"
---
# <span data-ttu-id="6b91a-101">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="6b91a-101">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="6b91a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b91a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b91a-103">Yerel bir Traffic Manager profil nesnesinden özel üst bilgi bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b91a-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b91a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b91a-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromProfile -Name <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b91a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b91a-105">DESCRIPTION</span></span>
<span data-ttu-id="6b91a-106">**Remove-AzureRmTrafficManagerCustomHeaderFromProfile** cmdlet 'i yerel bir Azure Traffic Manager profili nesnesinden özel üst bilgi bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b91a-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="6b91a-107">New-AzureRmTrafficManagerProfile veya Get-AzureRmTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b91a-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="6b91a-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="6b91a-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="6b91a-109">Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="6b91a-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="6b91a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b91a-110">EXAMPLES</span></span>

### <span data-ttu-id="6b91a-111">Örnek 1: profilden özel üst bilgi bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6b91a-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="6b91a-112">İlk komut **Get-AzureRmTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="6b91a-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="6b91a-113">İkinci komut $TrafficManagerProfile uygulamasında depolanan profilden özel başlık bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6b91a-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="6b91a-114">Son komutu, Traffic Manager 'daki profili $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6b91a-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="6b91a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b91a-115">PARAMETERS</span></span>

### <span data-ttu-id="6b91a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b91a-116">-DefaultProfile</span></span>
<span data-ttu-id="6b91a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b91a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b91a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b91a-118">-Name</span></span>
<span data-ttu-id="6b91a-119">Kaldırılacak özel üstbilgi bilgilerinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b91a-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="6b91a-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6b91a-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="6b91a-121">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b91a-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="6b91a-122">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6b91a-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="6b91a-123">**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6b91a-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="6b91a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b91a-124">-Confirm</span></span>
<span data-ttu-id="6b91a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b91a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b91a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b91a-126">-WhatIf</span></span>
<span data-ttu-id="6b91a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b91a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b91a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b91a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b91a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b91a-129">CommonParameters</span></span>
<span data-ttu-id="6b91a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b91a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b91a-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b91a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b91a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b91a-132">INPUTS</span></span>

### <span data-ttu-id="6b91a-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6b91a-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="6b91a-134">Bu cmdlet, bu cmdlet 'e bir **TrafficManagerProfile** nesnesi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="6b91a-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="6b91a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b91a-135">OUTPUTS</span></span>

### <span data-ttu-id="6b91a-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6b91a-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="6b91a-137">Bu cmdlet değiştirilmiş bir **TrafficManagerProfile** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="6b91a-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="6b91a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b91a-138">NOTES</span></span>

## <span data-ttu-id="6b91a-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b91a-139">RELATED LINKS</span></span>

[<span data-ttu-id="6b91a-140">Add-AzureRmTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="6b91a-140">Add-AzureRmTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="6b91a-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6b91a-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6b91a-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6b91a-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
