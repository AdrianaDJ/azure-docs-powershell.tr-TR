---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106227"
---
# <span data-ttu-id="a6403-101">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="a6403-101">New-AzureAffinityGroup</span></span>

## <span data-ttu-id="a6403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6403-102">SYNOPSIS</span></span>
<span data-ttu-id="a6403-103">Geçerli abonelikte bir benzeşim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6403-103">Creates an affinity group in the current subscription.</span></span>

## <span data-ttu-id="a6403-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6403-104">SYNTAX</span></span>

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6403-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6403-105">DESCRIPTION</span></span>
<span data-ttu-id="a6403-106">**New-AzureAffinityGroup** cmdlet 'i, geçerli Azure aboneliğinde bir Azure benzeşim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6403-106">The **New-AzureAffinityGroup** cmdlet creates an Azure affinity group in the current Azure subscription.</span></span>

<span data-ttu-id="a6403-107">Benzeşim grubu, hizmetlerinizin ve kaynaklarınızı bir Azure veri merkezinde bir araya getirir.</span><span class="sxs-lookup"><span data-stu-id="a6403-107">An affinity group puts your services and their resources together in an Azure datacenter.</span></span>
<span data-ttu-id="a6403-108">Benzeşim grubu, en iyi performans için üyeleri birlikte gruplar.</span><span class="sxs-lookup"><span data-stu-id="a6403-108">The affinity group groups members together for optimal performance.</span></span>
<span data-ttu-id="a6403-109">Abonelik düzeyinde benzeşim grupları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6403-109">Define affinity groups at the subscription level.</span></span>
<span data-ttu-id="a6403-110">Benzeşim gruplarınız, oluşturduğunuz sonraki bulut hizmetleri veya depolama hesapları tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a6403-110">Your affinity groups are available to any subsequent cloud services or storage accounts that you create.</span></span>
<span data-ttu-id="a6403-111">Bir benzeşim grubuna yalnızca oluşturduğunuzda hizmet ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6403-111">You can add services to an affinity group only when you create it.</span></span>

## <span data-ttu-id="a6403-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6403-112">EXAMPLES</span></span>

### <span data-ttu-id="a6403-113">Örnek 1: benzeşim grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="a6403-113">Example 1: Create an affinity group</span></span>
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

<span data-ttu-id="a6403-114">Bu komut, Güney Merkezi ABD bölgesinde South01 adlı bir benzeşim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6403-114">This command creates an affinity group named South01 in the South Central US region.</span></span>
<span data-ttu-id="a6403-115">Komut bir etiket ve açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6403-115">The command specifies a label and a description.</span></span>

## <span data-ttu-id="a6403-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6403-116">PARAMETERS</span></span>

### <span data-ttu-id="a6403-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a6403-117">-Description</span></span>
<span data-ttu-id="a6403-118">Benzeşim grubu için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6403-118">Specifies a description for the affinity group.</span></span>
<span data-ttu-id="a6403-119">Açıklama 1024 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="a6403-119">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="a6403-120">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a6403-120">-InformationAction</span></span>
<span data-ttu-id="a6403-121">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6403-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a6403-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a6403-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a6403-123">'A</span><span class="sxs-lookup"><span data-stu-id="a6403-123">Continue</span></span>
- <span data-ttu-id="a6403-124">Manıza</span><span class="sxs-lookup"><span data-stu-id="a6403-124">Ignore</span></span>
- <span data-ttu-id="a6403-125">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="a6403-125">Inquire</span></span>
- <span data-ttu-id="a6403-126">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="a6403-126">SilentlyContinue</span></span>
- <span data-ttu-id="a6403-127">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="a6403-127">Stop</span></span>
- <span data-ttu-id="a6403-128">Biliriz</span><span class="sxs-lookup"><span data-stu-id="a6403-128">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6403-129">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="a6403-129">-InformationVariable</span></span>
<span data-ttu-id="a6403-130">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6403-130">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6403-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a6403-131">-Label</span></span>
<span data-ttu-id="a6403-132">Benzeşim grubu için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6403-132">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="a6403-133">Etiket en çok 100 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="a6403-133">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="a6403-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="a6403-134">-Location</span></span>
<span data-ttu-id="a6403-135">Bu cmdlet 'in benzeşim grubunu oluşturduğu Azure Datacenter 'un coğrafi konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6403-135">Specifies the geographical location of the Azure datacenter where this cmdlet creates the affinity group.</span></span>

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

### <span data-ttu-id="a6403-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6403-136">-Name</span></span>
<span data-ttu-id="a6403-137">Benzeşim grubu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6403-137">Specifies a name for the affinity group.</span></span>
<span data-ttu-id="a6403-138">Ad, aboneliğe özgü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a6403-138">The name must be unique to the subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6403-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="a6403-139">-Profile</span></span>
<span data-ttu-id="a6403-140">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6403-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a6403-141">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a6403-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6403-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6403-142">CommonParameters</span></span>
<span data-ttu-id="a6403-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6403-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6403-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6403-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6403-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6403-145">INPUTS</span></span>

## <span data-ttu-id="a6403-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6403-146">OUTPUTS</span></span>

## <span data-ttu-id="a6403-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6403-147">NOTES</span></span>

## <span data-ttu-id="a6403-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6403-148">RELATED LINKS</span></span>

[<span data-ttu-id="a6403-149">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="a6403-149">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="a6403-150">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="a6403-150">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="a6403-151">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="a6403-151">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


