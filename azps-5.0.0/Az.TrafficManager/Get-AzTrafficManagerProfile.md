---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277902"
---
# <span data-ttu-id="d5595-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5595-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="d5595-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5595-102">SYNOPSIS</span></span>
<span data-ttu-id="d5595-103">Traffic Manager profilini alır.</span><span class="sxs-lookup"><span data-stu-id="d5595-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="d5595-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5595-104">SYNTAX</span></span>

### <span data-ttu-id="d5595-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5595-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5595-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5595-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5595-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5595-107">DESCRIPTION</span></span>
<span data-ttu-id="d5595-108">**Get-AzTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili alır ve bu profili temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d5595-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="d5595-109">Adını ve kaynak grubu adını kullanarak bir profil belirtin.</span><span class="sxs-lookup"><span data-stu-id="d5595-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="d5595-110">Bu nesneyi yerel olarak değiştirebilir ve Set-AzTrafficManagerProfile cmdlet 'ini kullanarak değişiklikleri profile uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5595-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="d5595-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5595-111">EXAMPLES</span></span>

### <span data-ttu-id="d5595-112">Örnek 1: profil alma</span><span class="sxs-lookup"><span data-stu-id="d5595-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d5595-113">Bu komut, ResourceGroup11 'daki ContosoProfile adlı profili alır.</span><span class="sxs-lookup"><span data-stu-id="d5595-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="d5595-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5595-114">PARAMETERS</span></span>

### <span data-ttu-id="d5595-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5595-115">-DefaultProfile</span></span>
<span data-ttu-id="d5595-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5595-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5595-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5595-117">-Name</span></span>
<span data-ttu-id="d5595-118">Bu cmdlet 'in aldığı Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5595-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d5595-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5595-119">-ResourceGroupName</span></span>
<span data-ttu-id="d5595-120">Bu cmdlet 'in aldığı Traffic Manager profilini içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5595-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d5595-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5595-121">CommonParameters</span></span>
<span data-ttu-id="d5595-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5595-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5595-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5595-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5595-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5595-124">INPUTS</span></span>

### <span data-ttu-id="d5595-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d5595-125">System.String</span></span>

## <span data-ttu-id="d5595-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5595-126">OUTPUTS</span></span>

### <span data-ttu-id="d5595-127">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5595-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d5595-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5595-128">NOTES</span></span>

## <span data-ttu-id="d5595-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5595-129">RELATED LINKS</span></span>

[<span data-ttu-id="d5595-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5595-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="d5595-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5595-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="d5595-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5595-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="d5595-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5595-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="d5595-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d5595-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


