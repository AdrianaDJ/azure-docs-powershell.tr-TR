---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324856"
---
# <span data-ttu-id="32dc1-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="32dc1-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="32dc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="32dc1-103">Yerel bir Traffic Manager profil nesnesine özel üstbilgi bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="32dc1-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="32dc1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32dc1-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32dc1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="32dc1-105">DESCRIPTION</span></span>
<span data-ttu-id="32dc1-106">**Add-AzTrafficManagerCustomHeaderToProfile** cmdlet 'i yerel bir Azure Traffic Manager profil nesnesine özel üstbilgi bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="32dc1-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="32dc1-107">New-AzTrafficManagerProfile veya Get-AzTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="32dc1-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="32dc1-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="32dc1-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="32dc1-109">Set-AzTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="32dc1-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="32dc1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32dc1-110">EXAMPLES</span></span>

### <span data-ttu-id="32dc1-111">Örnek 1: profile özel üst bilgi bilgileri ekleme</span><span class="sxs-lookup"><span data-stu-id="32dc1-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="32dc1-112">İlk komut **Get-AzTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="32dc1-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="32dc1-113">Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.</span><span class="sxs-lookup"><span data-stu-id="32dc1-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="32dc1-114">İkinci komut, $TrafficManagerProfile depolanan profile özel üstbilgi bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="32dc1-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="32dc1-115">Son komutu, Traffic Manager 'daki profili $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="32dc1-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="32dc1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32dc1-116">PARAMETERS</span></span>

### <span data-ttu-id="32dc1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32dc1-117">-DefaultProfile</span></span>
<span data-ttu-id="32dc1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32dc1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32dc1-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="32dc1-119">-Name</span></span>
<span data-ttu-id="32dc1-120">Eklenecek özel başlık bilgilerinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32dc1-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="32dc1-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="32dc1-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="32dc1-122">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="32dc1-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="32dc1-123">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="32dc1-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="32dc1-124">**TrafficManagerProfile** nesnesi almak için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="32dc1-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="32dc1-125">-Değer</span><span class="sxs-lookup"><span data-stu-id="32dc1-125">-Value</span></span>
<span data-ttu-id="32dc1-126">Eklenecek özel üstbilgi bilgilerinin değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32dc1-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="32dc1-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="32dc1-127">-Confirm</span></span>
<span data-ttu-id="32dc1-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32dc1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32dc1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32dc1-129">-WhatIf</span></span>
<span data-ttu-id="32dc1-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32dc1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32dc1-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="32dc1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32dc1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32dc1-132">CommonParameters</span></span>
<span data-ttu-id="32dc1-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32dc1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32dc1-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32dc1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32dc1-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32dc1-135">INPUTS</span></span>

### <span data-ttu-id="32dc1-136">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="32dc1-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="32dc1-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32dc1-137">OUTPUTS</span></span>

### <span data-ttu-id="32dc1-138">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="32dc1-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="32dc1-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32dc1-139">NOTES</span></span>

## <span data-ttu-id="32dc1-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32dc1-140">RELATED LINKS</span></span>

[<span data-ttu-id="32dc1-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="32dc1-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="32dc1-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="32dc1-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="32dc1-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="32dc1-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
