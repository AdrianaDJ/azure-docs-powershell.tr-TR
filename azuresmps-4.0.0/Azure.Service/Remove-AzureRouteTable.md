---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 58329D8A-CB54-46FB-84A7-C31F00C13827
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6333430682de7693b6b87f9d037dea66725bfed8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106132"
---
# <span data-ttu-id="0d9c6-101">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d9c6-101">Remove-AzureRouteTable</span></span>

## <span data-ttu-id="0d9c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="0d9c6-103">Yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-103">Removes a route table.</span></span>

## <span data-ttu-id="0d9c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d9c6-104">SYNTAX</span></span>

```
Remove-AzureRouteTable -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d9c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d9c6-105">DESCRIPTION</span></span>
<span data-ttu-id="0d9c6-106">**Remove-AzureRouteTable** cmdlet 'i aboneliğinizden bir yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-106">The **Remove-AzureRouteTable** cmdlet removes a route table from your subscription.</span></span>
<span data-ttu-id="0d9c6-107">Bir yol tablosu bir alt ağla ilişkilendirilmişse, tabloyu kaldıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-107">If a route table is associated to a subnet, you cannot remove the table.</span></span>

## <span data-ttu-id="0d9c6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d9c6-108">EXAMPLES</span></span>

### <span data-ttu-id="0d9c6-109">Örnek 1: yol tablosunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="0d9c6-109">Example 1: Remove a route table</span></span>
```
PS C:\> Remove-AzureRouteTable -Name "PublicRouteTable"
```

<span data-ttu-id="0d9c6-110">Bu komut, PublicRouteTable adlı yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-110">This command removes the route table named PublicRouteTable.</span></span>

## <span data-ttu-id="0d9c6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d9c6-111">PARAMETERS</span></span>

### <span data-ttu-id="0d9c6-112">-Force</span><span class="sxs-lookup"><span data-stu-id="0d9c6-112">-Force</span></span>
<span data-ttu-id="0d9c6-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0d9c6-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d9c6-114">-Name</span></span>
<span data-ttu-id="0d9c6-115">Bu cmdlet 'in kaldırıldığı yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-115">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d9c6-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0d9c6-116">-PassThru</span></span>
<span data-ttu-id="0d9c6-117">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d9c6-118">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d9c6-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="0d9c6-119">-Profile</span></span>
<span data-ttu-id="0d9c6-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0d9c6-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0d9c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d9c6-122">CommonParameters</span></span>
<span data-ttu-id="0d9c6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d9c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d9c6-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d9c6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d9c6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d9c6-125">INPUTS</span></span>

## <span data-ttu-id="0d9c6-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d9c6-126">OUTPUTS</span></span>

## <span data-ttu-id="0d9c6-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d9c6-127">NOTES</span></span>

## <span data-ttu-id="0d9c6-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d9c6-128">RELATED LINKS</span></span>

[<span data-ttu-id="0d9c6-129">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d9c6-129">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="0d9c6-130">Yeni-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d9c6-130">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)
