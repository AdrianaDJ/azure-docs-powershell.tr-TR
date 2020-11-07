---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: fe97e35c0b4b728601cc33888deb9afbdb0620b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932769"
---
# <span data-ttu-id="49ffb-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49ffb-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="49ffb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="49ffb-103">Traffic Manager profilini alır.</span><span class="sxs-lookup"><span data-stu-id="49ffb-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="49ffb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49ffb-104">SYNTAX</span></span>

### <span data-ttu-id="49ffb-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ffb-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49ffb-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ffb-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49ffb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="49ffb-107">DESCRIPTION</span></span>
<span data-ttu-id="49ffb-108">**Get-AzTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili alır ve bu profili temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="49ffb-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="49ffb-109">Adını ve kaynak grubu adını kullanarak bir profil belirtin.</span><span class="sxs-lookup"><span data-stu-id="49ffb-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="49ffb-110">Bu nesneyi yerel olarak değiştirebilir ve Set-AzTrafficManagerProfile cmdlet 'ini kullanarak değişiklikleri profile uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49ffb-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="49ffb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49ffb-111">EXAMPLES</span></span>

### <span data-ttu-id="49ffb-112">Örnek 1: profil alma</span><span class="sxs-lookup"><span data-stu-id="49ffb-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="49ffb-113">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="49ffb-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="49ffb-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49ffb-114">PARAMETERS</span></span>

### <span data-ttu-id="49ffb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ffb-115">-DefaultProfile</span></span>
<span data-ttu-id="49ffb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49ffb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49ffb-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="49ffb-117">-Name</span></span>
<span data-ttu-id="49ffb-118">Bu cmdlet 'in aldığı Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49ffb-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="49ffb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ffb-119">-ResourceGroupName</span></span>
<span data-ttu-id="49ffb-120">Bu cmdlet 'in aldığı Traffic Manager profilini içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49ffb-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="49ffb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ffb-121">CommonParameters</span></span>
<span data-ttu-id="49ffb-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49ffb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ffb-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ffb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ffb-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49ffb-124">INPUTS</span></span>

### <span data-ttu-id="49ffb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="49ffb-125">System.String</span></span>

## <span data-ttu-id="49ffb-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49ffb-126">OUTPUTS</span></span>

### <span data-ttu-id="49ffb-127">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49ffb-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="49ffb-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49ffb-128">NOTES</span></span>

## <span data-ttu-id="49ffb-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49ffb-129">RELATED LINKS</span></span>

[<span data-ttu-id="49ffb-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49ffb-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="49ffb-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49ffb-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="49ffb-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49ffb-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="49ffb-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49ffb-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="49ffb-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49ffb-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


