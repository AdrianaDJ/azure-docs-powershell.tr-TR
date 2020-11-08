---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105988"
---
# <span data-ttu-id="915e9-101">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="915e9-101">New-AzureSBNamespace</span></span>

## <span data-ttu-id="915e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="915e9-102">SYNOPSIS</span></span>
<span data-ttu-id="915e9-103">Ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="915e9-103">Creates a namespace.</span></span>

## <span data-ttu-id="915e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="915e9-104">SYNTAX</span></span>

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="915e9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="915e9-105">DESCRIPTION</span></span>
<span data-ttu-id="915e9-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="915e9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="915e9-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="915e9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="915e9-108">**New-AzureSBNamespace** cmdlet 'ı, Azure 'Daki hizmet veri yolu ile kullanmak için bir hizmet ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="915e9-108">The **New-AzureSBNamespace** cmdlet creates a service namespace for use with Service Bus in Azure.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="915e9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="915e9-109">EXAMPLES</span></span>

### <span data-ttu-id="915e9-110">Örnek 1: hizmet ad alanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="915e9-110">Example 1: Create a service namespace</span></span>
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

<span data-ttu-id="915e9-111">Örnekler, Azure 'daki hizmet veri yolu ile kullanmak için bir hizmet ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="915e9-111">The examples create a service namespace for use with Service Bus in Azure.</span></span>
<span data-ttu-id="915e9-112">Her iki örnek de gerekli parametre değerlerini içerir, ancak ilki parametre adlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="915e9-112">Both examples include the required parameter values, but only the first includes the parameter names.</span></span>
<span data-ttu-id="915e9-113">İkinci örnek, her iki parametre de konumsal olduğu ve değerleri gerekli sırayla verildiği için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="915e9-113">The second example can be used because both parameters are positional and their values are given in the required order.</span></span>

## <span data-ttu-id="915e9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="915e9-114">PARAMETERS</span></span>

### <span data-ttu-id="915e9-115">-CreateACSNamespace</span><span class="sxs-lookup"><span data-stu-id="915e9-115">-CreateACSNamespace</span></span>
<span data-ttu-id="915e9-116">Hizmet ad alanına ek olarak ilişkili bir ACS ad alanı oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="915e9-116">Specifies whether to create an associated ACS namespace in addition to the service namespace.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915e9-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="915e9-117">-Location</span></span>
<span data-ttu-id="915e9-118">Yeni ad alanı için bir bölge belirtir.</span><span class="sxs-lookup"><span data-stu-id="915e9-118">Specifies a region for the new namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915e9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="915e9-119">-Name</span></span>
<span data-ttu-id="915e9-120">Yeni ad alanı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="915e9-120">Specifies a name for the new namespace.</span></span>

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

### <span data-ttu-id="915e9-121">-NamespaceType</span><span class="sxs-lookup"><span data-stu-id="915e9-121">-NamespaceType</span></span>
<span data-ttu-id="915e9-122">Mesajlaşma veya bildirim hubları için ad boşluğunu kullanıp kullanmayacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="915e9-122">Specify a whether to use the namespace for Messaging or Notification Hubs.</span></span>

```yaml
Type: NamespaceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915e9-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="915e9-123">-Profile</span></span>
<span data-ttu-id="915e9-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="915e9-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="915e9-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="915e9-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="915e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="915e9-126">CommonParameters</span></span>
<span data-ttu-id="915e9-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="915e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="915e9-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="915e9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="915e9-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="915e9-129">INPUTS</span></span>

## <span data-ttu-id="915e9-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="915e9-130">OUTPUTS</span></span>

## <span data-ttu-id="915e9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="915e9-131">NOTES</span></span>

## <span data-ttu-id="915e9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="915e9-132">RELATED LINKS</span></span>

[<span data-ttu-id="915e9-133">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="915e9-133">Remove-AzureSBNamespace</span></span>](./Remove-AzureSBNamespace.md)


