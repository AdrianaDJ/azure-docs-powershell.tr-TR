---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: d8f4b5e069ef273dedc8e2e5a1f929d1649aefdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934383"
---
# <span data-ttu-id="be788-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be788-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="be788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be788-102">SYNOPSIS</span></span>
<span data-ttu-id="be788-103">Traffic Manager profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be788-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="be788-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be788-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be788-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be788-105">DESCRIPTION</span></span>
<span data-ttu-id="be788-106">**Set-AzTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be788-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="be788-107">Bu cmdlet profili yerel bir profil nesnesinden güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be788-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="be788-108">*TrafficManagerProfile* parametresini kullanarak veya ardışık düzeni kullanarak profil nesnesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="be788-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="be788-109">Get-AzTrafficManagerProfile cmdlet 'ini kullanarak bir profili temsil eden yerel bir nesne edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="be788-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="be788-110">Nesneyi yerel olarak değiştirip değişikliklerinizi kaydetmek için **set-AzTrafficManagerProfile** kullanın.</span><span class="sxs-lookup"><span data-stu-id="be788-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="be788-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be788-111">EXAMPLES</span></span>

### <span data-ttu-id="be788-112">Örnek 1: profili güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="be788-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="be788-113">İlk komut, Get-AzTrafficManagerProfile cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="be788-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="be788-114">Komut, profili yerel olarak $TrafficManagerProfile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="be788-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="be788-115">İkinci komut bu profili yerel olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="be788-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="be788-116">Bu komut profili devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="be788-116">This command disables the profile.</span></span>

<span data-ttu-id="be788-117">Üçüncü komut, ContosoProfile adlı Traffic Manager profilini $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be788-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="be788-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be788-118">PARAMETERS</span></span>

### <span data-ttu-id="be788-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be788-119">-DefaultProfile</span></span>
<span data-ttu-id="be788-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be788-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be788-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be788-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="be788-122">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="be788-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="be788-123">Bu cmdlet, Traffic Manager 'ı bu yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be788-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="be788-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be788-124">CommonParameters</span></span>
<span data-ttu-id="be788-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be788-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be788-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be788-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be788-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be788-127">INPUTS</span></span>

### <span data-ttu-id="be788-128">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be788-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="be788-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be788-129">OUTPUTS</span></span>

### <span data-ttu-id="be788-130">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be788-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="be788-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be788-131">NOTES</span></span>

## <span data-ttu-id="be788-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be788-132">RELATED LINKS</span></span>

[<span data-ttu-id="be788-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="be788-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="be788-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be788-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="be788-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be788-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="be788-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="be788-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="be788-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="be788-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


