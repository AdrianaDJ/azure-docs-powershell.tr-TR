---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: e8baf033131442f23a0db63339673018b209f140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763080"
---
# <span data-ttu-id="49359-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49359-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="49359-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49359-102">SYNOPSIS</span></span>
<span data-ttu-id="49359-103">Traffic Manager profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="49359-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49359-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49359-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49359-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49359-105">DESCRIPTION</span></span>
<span data-ttu-id="49359-106">**Set-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profilini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="49359-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="49359-107">Bu cmdlet profili yerel bir profil nesnesinden güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="49359-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="49359-108">*TrafficManagerProfile* parametresini kullanarak veya ardışık düzeni kullanarak profil nesnesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49359-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="49359-109">Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak bir profili temsil eden yerel bir nesne edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49359-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="49359-110">Nesneyi yerel olarak değiştirip değişikliklerinizi kaydetmek için **set-AzureRmTrafficManagerProfile** kullanın.</span><span class="sxs-lookup"><span data-stu-id="49359-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="49359-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49359-111">EXAMPLES</span></span>

### <span data-ttu-id="49359-112">Örnek 1: profili güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="49359-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="49359-113">İlk komut, Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="49359-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="49359-114">Komut, profili yerel olarak $TrafficManagerProfile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="49359-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="49359-115">İkinci komut bu profili yerel olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="49359-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="49359-116">Bu komut profili devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="49359-116">This command disables the profile.</span></span>

<span data-ttu-id="49359-117">Üçüncü komut, ContosoProfile adlı Traffic Manager profilini $TrafficManagerProfile yerel değeri eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="49359-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="49359-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49359-118">PARAMETERS</span></span>

### <span data-ttu-id="49359-119">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49359-119">-TrafficManagerProfile</span></span>
<span data-ttu-id="49359-120">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="49359-120">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="49359-121">Bu cmdlet, Traffic Manager 'ı bu yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="49359-121">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="49359-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49359-122">-DefaultProfile</span></span>
<span data-ttu-id="49359-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49359-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49359-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49359-124">CommonParameters</span></span>
<span data-ttu-id="49359-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49359-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49359-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49359-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49359-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49359-127">INPUTS</span></span>

### <span data-ttu-id="49359-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49359-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="49359-129">Bu cmdlet bir **TrafficManagerProfile** nesnesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="49359-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="49359-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49359-130">OUTPUTS</span></span>

### <span data-ttu-id="49359-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49359-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="49359-132">Bu cmdlet bir **TrafficManagerProfile** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="49359-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="49359-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49359-133">NOTES</span></span>

## <span data-ttu-id="49359-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49359-134">RELATED LINKS</span></span>

[<span data-ttu-id="49359-135">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="49359-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="49359-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49359-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="49359-137">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49359-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="49359-138">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="49359-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="49359-139">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49359-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)


