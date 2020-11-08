---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F4BADE88-28A2-42FB-9578-93D65148709E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f73e47ec25d44d3965279066de98585ae2cbaee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105989"
---
# <span data-ttu-id="6d747-101">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d747-101">New-AzureRouteTable</span></span>

## <span data-ttu-id="6d747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d747-102">SYNOPSIS</span></span>
<span data-ttu-id="6d747-103">Yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d747-103">Creates a route table.</span></span>

## <span data-ttu-id="6d747-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d747-104">SYNTAX</span></span>

```
New-AzureRouteTable -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d747-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d747-105">DESCRIPTION</span></span>
<span data-ttu-id="6d747-106">**New-AzureRouteTable** cmdlet 'i belirtilen konumda bir yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d747-106">The **New-AzureRouteTable** cmdlet creates a route table in a specified location.</span></span>
<span data-ttu-id="6d747-107">Yönlendirme tablosuna Kullanıcı tanımlı yollar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d747-107">You can add user-defined routes to the route table.</span></span>
<span data-ttu-id="6d747-108">Yol tablosunu sanal ağdaki bir alt ağla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d747-108">You can associate the route table to a subnet in a virtual network.</span></span>

## <span data-ttu-id="6d747-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d747-109">EXAMPLES</span></span>

## <span data-ttu-id="6d747-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d747-110">PARAMETERS</span></span>

### <span data-ttu-id="6d747-111">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6d747-111">-Label</span></span>
<span data-ttu-id="6d747-112">Yeni yol tablosu için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d747-112">Specifies a description for the new route table.</span></span>

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

### <span data-ttu-id="6d747-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="6d747-113">-Location</span></span>
<span data-ttu-id="6d747-114">Bu cmdlet 'in yol tablosunu oluşturduğu konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d747-114">Specifies the location in which this cmdlet creates the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d747-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d747-115">-Name</span></span>
<span data-ttu-id="6d747-116">Bu cmdlet 'in oluşturduğu yol tablosu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d747-116">Specifies a name for the route table that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d747-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="6d747-117">-Profile</span></span>
<span data-ttu-id="6d747-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d747-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6d747-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6d747-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6d747-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d747-120">CommonParameters</span></span>
<span data-ttu-id="6d747-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d747-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d747-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d747-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d747-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d747-123">INPUTS</span></span>

## <span data-ttu-id="6d747-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d747-124">OUTPUTS</span></span>

## <span data-ttu-id="6d747-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d747-125">NOTES</span></span>

## <span data-ttu-id="6d747-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d747-126">RELATED LINKS</span></span>

[<span data-ttu-id="6d747-127">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d747-127">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="6d747-128">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d747-128">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


