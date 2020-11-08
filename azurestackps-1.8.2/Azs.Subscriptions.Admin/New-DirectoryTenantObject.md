---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106850"
---
# <span data-ttu-id="28917-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="28917-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="28917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28917-102">SYNOPSIS</span></span>
<span data-ttu-id="28917-103">Dizin kiracısı.</span><span class="sxs-lookup"><span data-stu-id="28917-103">Directory tenant.</span></span>

## <span data-ttu-id="28917-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28917-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="28917-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="28917-105">DESCRIPTION</span></span>
<span data-ttu-id="28917-106">Dizin kiracısı.</span><span class="sxs-lookup"><span data-stu-id="28917-106">Directory tenant.</span></span>

## <span data-ttu-id="28917-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28917-107">EXAMPLES</span></span>

### <span data-ttu-id="28917-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="28917-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="28917-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="28917-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="28917-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28917-110">PARAMETERS</span></span>

### <span data-ttu-id="28917-111">-ID</span><span class="sxs-lookup"><span data-stu-id="28917-111">-Id</span></span>
<span data-ttu-id="28917-112">Kaynağın URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="28917-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28917-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="28917-113">-Location</span></span>
<span data-ttu-id="28917-114">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="28917-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28917-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="28917-115">-Name</span></span>
<span data-ttu-id="28917-116">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="28917-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28917-117">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="28917-117">-Tags</span></span>
<span data-ttu-id="28917-118">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="28917-118">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28917-119">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="28917-119">-TenantId</span></span>
<span data-ttu-id="28917-120">Kiracıya benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="28917-120">Tenant unique identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28917-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="28917-121">-Type</span></span>
<span data-ttu-id="28917-122">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="28917-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28917-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28917-123">CommonParameters</span></span>
<span data-ttu-id="28917-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28917-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28917-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28917-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28917-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28917-126">INPUTS</span></span>

## <span data-ttu-id="28917-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28917-127">OUTPUTS</span></span>

## <span data-ttu-id="28917-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28917-128">NOTES</span></span>

## <span data-ttu-id="28917-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28917-129">RELATED LINKS</span></span>

