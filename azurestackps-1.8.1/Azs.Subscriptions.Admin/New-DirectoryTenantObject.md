---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934908"
---
# <span data-ttu-id="c625f-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="c625f-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="c625f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c625f-102">SYNOPSIS</span></span>
<span data-ttu-id="c625f-103">Dizin kiracısı.</span><span class="sxs-lookup"><span data-stu-id="c625f-103">Directory tenant.</span></span>

## <span data-ttu-id="c625f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c625f-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c625f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c625f-105">DESCRIPTION</span></span>
<span data-ttu-id="c625f-106">Dizin kiracısı.</span><span class="sxs-lookup"><span data-stu-id="c625f-106">Directory tenant.</span></span>

## <span data-ttu-id="c625f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c625f-107">EXAMPLES</span></span>

### <span data-ttu-id="c625f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c625f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c625f-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="c625f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c625f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c625f-110">PARAMETERS</span></span>

### <span data-ttu-id="c625f-111">-ID</span><span class="sxs-lookup"><span data-stu-id="c625f-111">-Id</span></span>
<span data-ttu-id="c625f-112">Kaynağın URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="c625f-112">URI of the resource.</span></span>

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

### <span data-ttu-id="c625f-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="c625f-113">-Location</span></span>
<span data-ttu-id="c625f-114">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="c625f-114">Location of the resource.</span></span>

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

### <span data-ttu-id="c625f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c625f-115">-Name</span></span>
<span data-ttu-id="c625f-116">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="c625f-116">Name of the resource.</span></span>

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

### <span data-ttu-id="c625f-117">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="c625f-117">-Tags</span></span>
<span data-ttu-id="c625f-118">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="c625f-118">List of key-value pairs.</span></span>

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

### <span data-ttu-id="c625f-119">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="c625f-119">-TenantId</span></span>
<span data-ttu-id="c625f-120">Kiracıya benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="c625f-120">Tenant unique identifier.</span></span>

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

### <span data-ttu-id="c625f-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="c625f-121">-Type</span></span>
<span data-ttu-id="c625f-122">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="c625f-122">Type of resource.</span></span>

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

### <span data-ttu-id="c625f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c625f-123">CommonParameters</span></span>
<span data-ttu-id="c625f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c625f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c625f-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c625f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c625f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c625f-126">INPUTS</span></span>

## <span data-ttu-id="c625f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c625f-127">OUTPUTS</span></span>

## <span data-ttu-id="c625f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c625f-128">NOTES</span></span>

## <span data-ttu-id="c625f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c625f-129">RELATED LINKS</span></span>

