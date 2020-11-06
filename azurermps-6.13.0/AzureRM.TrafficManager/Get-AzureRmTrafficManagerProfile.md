---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 239e0147b1955c59dbe34591f85273f05aa12c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587111"
---
# <span data-ttu-id="0b2fc-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0b2fc-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="0b2fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2fc-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2fc-103">Traffic Manager profilini alır.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b2fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b2fc-104">SYNTAX</span></span>

### <span data-ttu-id="0b2fc-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b2fc-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b2fc-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b2fc-106">AccountNameParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b2fc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b2fc-107">DESCRIPTION</span></span>
<span data-ttu-id="0b2fc-108">**Get-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili alır ve bu profili temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-108">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="0b2fc-109">Adını ve kaynak grubu adını kullanarak bir profil belirtin.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="0b2fc-110">Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak değişiklikleri profile uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="0b2fc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b2fc-111">EXAMPLES</span></span>

### <span data-ttu-id="0b2fc-112">Örnek 1: profil alma</span><span class="sxs-lookup"><span data-stu-id="0b2fc-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0b2fc-113">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="0b2fc-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b2fc-114">PARAMETERS</span></span>

### <span data-ttu-id="0b2fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2fc-115">-DefaultProfile</span></span>
<span data-ttu-id="0b2fc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b2fc-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b2fc-117">-Name</span></span>
<span data-ttu-id="0b2fc-118">Bu cmdlet 'in aldığı Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2fc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2fc-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b2fc-120">Bu cmdlet 'in aldığı Traffic Manager profilini içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2fc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2fc-121">CommonParameters</span></span>
<span data-ttu-id="0b2fc-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2fc-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2fc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2fc-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b2fc-124">INPUTS</span></span>

### <span data-ttu-id="0b2fc-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0b2fc-125">None</span></span>
<span data-ttu-id="0b2fc-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b2fc-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b2fc-127">OUTPUTS</span></span>

### <span data-ttu-id="0b2fc-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0b2fc-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="0b2fc-129">Bu cmdlet bir **TrafficManagerProfile** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-129">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="0b2fc-130">Bu nesneyi değiştirebilir ve ardından **set-AzureRmTrafficManagerProfile** kullanarak Traffic Manager 'a değişiklikleri uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b2fc-130">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="0b2fc-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b2fc-131">NOTES</span></span>

## <span data-ttu-id="0b2fc-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b2fc-132">RELATED LINKS</span></span>

[<span data-ttu-id="0b2fc-133">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0b2fc-133">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0b2fc-134">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0b2fc-134">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0b2fc-135">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0b2fc-135">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0b2fc-136">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0b2fc-136">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0b2fc-137">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0b2fc-137">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


