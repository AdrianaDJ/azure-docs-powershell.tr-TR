---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5C8A79D1-32D4-4B30-AAC8-C6EF3B68017E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c2f695022e3a03d90443ad9ac2eb36ef8cb22ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106135"
---
# <span data-ttu-id="a8a02-101">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="a8a02-101">Remove-AzureRoute</span></span>

## <span data-ttu-id="a8a02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8a02-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a02-103">Yol tablosundan bir yol kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a8a02-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="a8a02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8a02-104">SYNTAX</span></span>

```
Remove-AzureRoute -RouteName <String> [-Force] -RouteTable <IRouteTable> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8a02-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8a02-105">DESCRIPTION</span></span>
<span data-ttu-id="a8a02-106">**Remove-AzureRoute** cmdlet 'i, yol tablosundan bir yol kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a8a02-106">The **Remove-AzureRoute** cmdlet removes a route from a route table.</span></span>

## <span data-ttu-id="a8a02-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8a02-107">EXAMPLES</span></span>

### <span data-ttu-id="a8a02-108">Örnek 1: rotayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="a8a02-108">Example 1: Remove a route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Remove-AzureRoute -RouteName "InternetRoute"
Confirm
Are you sure you want to remove the Route "InternetRoute" from Route Table "ApplianceRouteTable"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="a8a02-109">Bu komut, ApplianceRouteTable adlı bir yol tablosu alır.</span><span class="sxs-lookup"><span data-stu-id="a8a02-109">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="a8a02-110">Komut bu yol tablosunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="a8a02-110">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="a8a02-111">Geçerli cmdlet, ınternetroute adlı bir yolu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a8a02-111">The current cmdlet removes a route named InternetRoute.</span></span>

## <span data-ttu-id="a8a02-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8a02-112">PARAMETERS</span></span>

### <span data-ttu-id="a8a02-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a8a02-113">-Force</span></span>
<span data-ttu-id="a8a02-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a8a02-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8a02-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8a02-115">-Profile</span></span>
<span data-ttu-id="a8a02-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8a02-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a8a02-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a8a02-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8a02-118">-RouteName</span><span class="sxs-lookup"><span data-stu-id="a8a02-118">-RouteName</span></span>
<span data-ttu-id="a8a02-119">Bu cmdlet 'in kaldırıldığı yeni yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8a02-119">Specifies a name for the new route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8a02-120">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a8a02-120">-RouteTable</span></span>
<span data-ttu-id="a8a02-121">Bu cmdlet 'in yolu kaldıran yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8a02-121">Specifies the route table from which this cmdlet removes a route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8a02-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a02-122">CommonParameters</span></span>
<span data-ttu-id="a8a02-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8a02-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a02-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8a02-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a02-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8a02-125">INPUTS</span></span>

## <span data-ttu-id="a8a02-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8a02-126">OUTPUTS</span></span>

## <span data-ttu-id="a8a02-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8a02-127">NOTES</span></span>

## <span data-ttu-id="a8a02-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8a02-128">RELATED LINKS</span></span>

[<span data-ttu-id="a8a02-129">Set-Azurlifute</span><span class="sxs-lookup"><span data-stu-id="a8a02-129">Set-AzureRoute</span></span>](./Set-AzureRoute.md)


