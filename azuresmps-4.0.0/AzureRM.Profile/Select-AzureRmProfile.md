---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571905"
---
# <span data-ttu-id="a31d5-101">Select-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="a31d5-101">Select-AzureRmProfile</span></span>

## <span data-ttu-id="a31d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a31d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a31d5-103">Azure kimlik doğrulama bilgilerini dosyadan yükler.</span><span class="sxs-lookup"><span data-stu-id="a31d5-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="a31d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a31d5-104">SYNTAX</span></span>

### <span data-ttu-id="a31d5-105">Inmemoryprofile</span><span class="sxs-lookup"><span data-stu-id="a31d5-105">InMemoryProfile</span></span>
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### <span data-ttu-id="a31d5-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="a31d5-106">ProfileFromDisk</span></span>
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## <span data-ttu-id="a31d5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a31d5-107">DESCRIPTION</span></span>
<span data-ttu-id="a31d5-108">Select-AzureRmProfile cmdlet, Azure ortamı ve bağlamını ayarlamak için bir dosyadan kimlik doğrulama bilgilerini yükler.</span><span class="sxs-lookup"><span data-stu-id="a31d5-108">The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="a31d5-109">Geçerli oturumda çalıştırdığınız cmdlet 'ler, Azure Resource Manager 'daki isteklerin kimlik doğrulaması için bu bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="a31d5-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="a31d5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a31d5-110">EXAMPLES</span></span>

### <span data-ttu-id="a31d5-111">Örnek 1: PSAzureProfile 'dan bir profil seçme</span><span class="sxs-lookup"><span data-stu-id="a31d5-111">Example 1: Selecting a profile from a PSAzureProfile</span></span>
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="a31d5-112">Bu örnek, bir PSAzureProfile 'dan cmdlet 'e geçirilen bir profil seçer.</span><span class="sxs-lookup"><span data-stu-id="a31d5-112">This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="a31d5-113">Örnek 2: JSON dosyasından bir profil seçme</span><span class="sxs-lookup"><span data-stu-id="a31d5-113">Example 2: Selecting a profile from a JSON file</span></span>
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="a31d5-114">Bu örnek, cmdlet 'e geçirilen JSON dosyasından bir profil seçer.</span><span class="sxs-lookup"><span data-stu-id="a31d5-114">This example selects a profile from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="a31d5-115">Bu JSON dosyası Save-Azurermprofıle içinden oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="a31d5-115">This JSON file can be created from Save-AzureRmProfile.</span></span>

## <span data-ttu-id="a31d5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a31d5-116">PARAMETERS</span></span>

### <span data-ttu-id="a31d5-117">-Yol</span><span class="sxs-lookup"><span data-stu-id="a31d5-117">-Path</span></span>
<span data-ttu-id="a31d5-118">Save-AzureRMProfile kullanılarak kaydedilen profil bilgilerinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a31d5-118">Specifies the path to profile information saved by using Save-AzureRMProfile.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31d5-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="a31d5-119">-Profile</span></span>
<span data-ttu-id="a31d5-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a31d5-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a31d5-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a31d5-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31d5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31d5-122">CommonParameters</span></span>
<span data-ttu-id="a31d5-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a31d5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31d5-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31d5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31d5-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a31d5-125">INPUTS</span></span>

## <span data-ttu-id="a31d5-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a31d5-126">OUTPUTS</span></span>

### <span data-ttu-id="a31d5-127">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a31d5-127">PSAzureProfile</span></span>

## <span data-ttu-id="a31d5-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a31d5-128">NOTES</span></span>

## <span data-ttu-id="a31d5-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a31d5-129">RELATED LINKS</span></span>

[<span data-ttu-id="a31d5-130">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="a31d5-130">Get-AzureRMContext</span></span>]()

