---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7F8C2223-5F82-4E4E-8057-44B72F7D5803
online version: ''
schema: 2.0.0
ms.openlocfilehash: a02d80d46696ff635da95c6bc29875f697f65fd4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106313"
---
# <span data-ttu-id="bfe9d-101">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="bfe9d-101">Get-AzureRouteTable</span></span>

## <span data-ttu-id="bfe9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfe9d-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe9d-103">Yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="bfe9d-103">Gets a route table.</span></span>

## <span data-ttu-id="bfe9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfe9d-104">SYNTAX</span></span>

```
Get-AzureRouteTable [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bfe9d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfe9d-105">DESCRIPTION</span></span>
<span data-ttu-id="bfe9d-106">**Get-AzureRouteTable** cmdlet 'i bir yol tablosu alır.</span><span class="sxs-lookup"><span data-stu-id="bfe9d-106">The **Get-AzureRouteTable** cmdlet gets a route table.</span></span>
<span data-ttu-id="bfe9d-107">Yol tablosundaki yolları listelemek için *ayrıntılı* parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="bfe9d-107">Specify the *Detailed* parameter to list the routes in the route table.</span></span>

## <span data-ttu-id="bfe9d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfe9d-108">EXAMPLES</span></span>

### <span data-ttu-id="bfe9d-109">Örnek 1: yol tablosunun ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="bfe9d-109">Example 1: Get details of a route table</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    ApplianceRouteTable           Central US                    Appliance Route Table
```

<span data-ttu-id="bfe9d-110">Bu komut, ApplianceRouteTable adlı bir yol tablosunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="bfe9d-110">This command gets the details of a route table named ApplianceRouteTable.</span></span>

## <span data-ttu-id="bfe9d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfe9d-111">PARAMETERS</span></span>

### <span data-ttu-id="bfe9d-112">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="bfe9d-112">-Detailed</span></span>
<span data-ttu-id="bfe9d-113">Bu cmdlet 'in yol tablosundaki yolları görüntüleyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bfe9d-113">Indicates that this cmdlet displays the routes in the route table.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfe9d-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="bfe9d-114">-Name</span></span>
<span data-ttu-id="bfe9d-115">Bu cmdlet 'in aldığı yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe9d-115">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bfe9d-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="bfe9d-116">-Profile</span></span>
<span data-ttu-id="bfe9d-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe9d-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bfe9d-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="bfe9d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bfe9d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe9d-119">CommonParameters</span></span>
<span data-ttu-id="bfe9d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfe9d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe9d-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfe9d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe9d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfe9d-122">INPUTS</span></span>

## <span data-ttu-id="bfe9d-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfe9d-123">OUTPUTS</span></span>

## <span data-ttu-id="bfe9d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfe9d-124">NOTES</span></span>

## <span data-ttu-id="bfe9d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfe9d-125">RELATED LINKS</span></span>

[<span data-ttu-id="bfe9d-126">Yeni-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="bfe9d-126">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="bfe9d-127">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="bfe9d-127">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


