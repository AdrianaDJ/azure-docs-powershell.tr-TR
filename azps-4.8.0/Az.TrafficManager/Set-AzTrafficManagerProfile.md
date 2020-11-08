---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268920"
---
# <span data-ttu-id="39456-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39456-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="39456-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39456-102">SYNOPSIS</span></span>
<span data-ttu-id="39456-103">Traffic Manager profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="39456-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="39456-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39456-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39456-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="39456-105">DESCRIPTION</span></span>
<span data-ttu-id="39456-106">**Set-AzTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="39456-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="39456-107">Bu cmdlet profili yerel bir profil nesnesinden güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="39456-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="39456-108">*TrafficManagerProfile* parametresini kullanarak veya ardışık düzeni kullanarak profil nesnesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="39456-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="39456-109">Get-AzTrafficManagerProfile cmdlet 'ini kullanarak bir profili temsil eden yerel bir nesne edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="39456-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="39456-110">Nesneyi yerel olarak değiştirip değişikliklerinizi kaydetmek için **set-AzTrafficManagerProfile** kullanın.</span><span class="sxs-lookup"><span data-stu-id="39456-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="39456-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39456-111">EXAMPLES</span></span>

### <span data-ttu-id="39456-112">Örnek 1: profili güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="39456-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="39456-113">İlk komut, Get-AzTrafficManagerProfile cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="39456-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="39456-114">Komut, profili yerel olarak $TrafficManagerProfile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="39456-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="39456-115">İkinci komut bu profili yerel olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="39456-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="39456-116">Bu komut profili devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="39456-116">This command disables the profile.</span></span>

<span data-ttu-id="39456-117">Üçüncü komut, ContosoProfile adlı Traffic Manager profilini $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="39456-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="39456-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39456-118">PARAMETERS</span></span>

### <span data-ttu-id="39456-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39456-119">-DefaultProfile</span></span>
<span data-ttu-id="39456-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39456-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39456-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39456-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="39456-122">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="39456-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="39456-123">Bu cmdlet, Traffic Manager 'ı bu yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="39456-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="39456-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39456-124">CommonParameters</span></span>
<span data-ttu-id="39456-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39456-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39456-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39456-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39456-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39456-127">INPUTS</span></span>

### <span data-ttu-id="39456-128">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39456-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="39456-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39456-129">OUTPUTS</span></span>

### <span data-ttu-id="39456-130">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39456-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="39456-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39456-131">NOTES</span></span>

## <span data-ttu-id="39456-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39456-132">RELATED LINKS</span></span>

[<span data-ttu-id="39456-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="39456-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="39456-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39456-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="39456-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39456-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="39456-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="39456-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="39456-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39456-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


