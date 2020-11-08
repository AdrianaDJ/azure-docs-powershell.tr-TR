---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106263"
---
# <span data-ttu-id="956e2-101">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="956e2-101">Get-WAPackVNet</span></span>

## <span data-ttu-id="956e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="956e2-102">SYNOPSIS</span></span>
<span data-ttu-id="956e2-103">Sanal ağları alır.</span><span class="sxs-lookup"><span data-stu-id="956e2-103">Gets virtual networks.</span></span>

## <span data-ttu-id="956e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="956e2-104">SYNTAX</span></span>

### <span data-ttu-id="956e2-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="956e2-105">Empty (Default)</span></span>
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="956e2-106">FromId</span><span class="sxs-lookup"><span data-stu-id="956e2-106">FromId</span></span>
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="956e2-107">FromName</span><span class="sxs-lookup"><span data-stu-id="956e2-107">FromName</span></span>
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="956e2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="956e2-108">DESCRIPTION</span></span>
<span data-ttu-id="956e2-109">**Get-WAPackVNet** cmdlet 'i sanal ağları alır.</span><span class="sxs-lookup"><span data-stu-id="956e2-109">The **Get-WAPackVNet** cmdlet gets virtual networks.</span></span>

## <span data-ttu-id="956e2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="956e2-110">EXAMPLES</span></span>

### <span data-ttu-id="956e2-111">Örnek 1: tüm sanal ağları alma</span><span class="sxs-lookup"><span data-stu-id="956e2-111">Example 1: Get all virtual networks</span></span>
```
PS C:\> Get-WAPackVNet
```

<span data-ttu-id="956e2-112">Bu komut tüm sanal ağları alır.</span><span class="sxs-lookup"><span data-stu-id="956e2-112">This command gets all virtual networks.</span></span>

### <span data-ttu-id="956e2-113">Örnek 2: KIMLIK kullanarak sanal ağ alma</span><span class="sxs-lookup"><span data-stu-id="956e2-113">Example 2: Get a virtual network by using an ID</span></span>
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="956e2-114">Bu komut belirtilen KIMLIĞE sahip sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="956e2-114">This command gets the virtual network that has the specified ID.</span></span>

### <span data-ttu-id="956e2-115">Örnek 3: ad kullanarak sanal ağ alma</span><span class="sxs-lookup"><span data-stu-id="956e2-115">Example 3: Get a virtual network by using a name</span></span>
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

<span data-ttu-id="956e2-116">Bu komut, ContosoVNet08 adındaki sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="956e2-116">This command gets the virtual network named ContosoVNet08.</span></span>

## <span data-ttu-id="956e2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="956e2-117">PARAMETERS</span></span>

### <span data-ttu-id="956e2-118">-ID</span><span class="sxs-lookup"><span data-stu-id="956e2-118">-ID</span></span>
<span data-ttu-id="956e2-119">Sanal ağın benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="956e2-119">Specifies the unique ID of a virtual network.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956e2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="956e2-120">-Name</span></span>
<span data-ttu-id="956e2-121">Sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="956e2-121">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956e2-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="956e2-122">-Profile</span></span>
<span data-ttu-id="956e2-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="956e2-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="956e2-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="956e2-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956e2-125">CommonParameters</span></span>
<span data-ttu-id="956e2-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="956e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956e2-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="956e2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956e2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="956e2-128">INPUTS</span></span>

## <span data-ttu-id="956e2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="956e2-129">OUTPUTS</span></span>

## <span data-ttu-id="956e2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="956e2-130">NOTES</span></span>

## <span data-ttu-id="956e2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="956e2-131">RELATED LINKS</span></span>

