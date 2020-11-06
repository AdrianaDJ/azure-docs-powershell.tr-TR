---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bdfe37622db49c554f128714ab2af65a11fbfce7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592371"
---
# <span data-ttu-id="1f390-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f390-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="1f390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f390-102">SYNOPSIS</span></span>
<span data-ttu-id="1f390-103">Traffic Manager profilini alır.</span><span class="sxs-lookup"><span data-stu-id="1f390-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f390-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f390-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f390-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f390-105">DESCRIPTION</span></span>
<span data-ttu-id="1f390-106">**Get-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili alır ve bu profili temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1f390-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="1f390-107">Adını ve kaynak grubu adını kullanarak bir profil belirtin.</span><span class="sxs-lookup"><span data-stu-id="1f390-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="1f390-108">Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak değişiklikleri profile uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f390-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="1f390-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f390-109">EXAMPLES</span></span>

### <span data-ttu-id="1f390-110">Örnek 1: profil alma</span><span class="sxs-lookup"><span data-stu-id="1f390-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1f390-111">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="1f390-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="1f390-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f390-112">PARAMETERS</span></span>

### <span data-ttu-id="1f390-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f390-113">-DefaultProfile</span></span>
<span data-ttu-id="1f390-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f390-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f390-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f390-115">-Name</span></span>
<span data-ttu-id="1f390-116">Bu cmdlet 'in aldığı Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f390-116">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f390-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f390-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f390-118">Bu cmdlet 'in aldığı Traffic Manager profilini içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f390-118">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f390-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f390-119">CommonParameters</span></span>
<span data-ttu-id="1f390-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f390-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f390-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f390-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f390-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f390-122">INPUTS</span></span>

### <span data-ttu-id="1f390-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1f390-123">None</span></span>
<span data-ttu-id="1f390-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1f390-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f390-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f390-125">OUTPUTS</span></span>

### <span data-ttu-id="1f390-126">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f390-126">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="1f390-127">Bu cmdlet bir **TrafficManagerProfile** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="1f390-127">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1f390-128">Bu nesneyi değiştirebilir ve ardından **set-AzureRmTrafficManagerProfile** kullanarak Traffic Manager 'a değişiklikleri uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f390-128">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="1f390-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f390-129">NOTES</span></span>

## <span data-ttu-id="1f390-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f390-130">RELATED LINKS</span></span>

[<span data-ttu-id="1f390-131">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f390-131">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1f390-132">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f390-132">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1f390-133">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f390-133">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1f390-134">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f390-134">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1f390-135">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f390-135">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


