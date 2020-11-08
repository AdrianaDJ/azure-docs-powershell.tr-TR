---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105899"
---
# <span data-ttu-id="d5e5e-101">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="d5e5e-101">New-AzureService</span></span>

## <span data-ttu-id="d5e5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e5e-103">Azure hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-103">Creates an Azure service.</span></span>

## <span data-ttu-id="d5e5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5e5e-104">SYNTAX</span></span>

### <span data-ttu-id="d5e5e-105">ParameterSetAffinityGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d5e5e-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d5e5e-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="d5e5e-106">ParameterSetLocation</span></span>
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d5e5e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5e5e-107">DESCRIPTION</span></span>
<span data-ttu-id="d5e5e-108">**New-AzureService** cmdlet 'i geçerli abonelikte yeni bir Azure hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-108">The **New-AzureService** cmdlet creates a new Azure service in the current subscription.</span></span>

## <span data-ttu-id="d5e5e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5e5e-109">EXAMPLES</span></span>

### <span data-ttu-id="d5e5e-110">Örnek 1: hizmet oluşturma</span><span class="sxs-lookup"><span data-stu-id="d5e5e-110">Example 1: Create a service</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

<span data-ttu-id="d5e5e-111">Bu komut, Güney Merkezi ABD 'de MySvc01 adlı yeni bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-111">This command creates a new service named MySvc01 in the South Central US location.</span></span>

### <span data-ttu-id="d5e5e-112">Örnek 2: benzeşim grubunda hizmet oluşturma</span><span class="sxs-lookup"><span data-stu-id="d5e5e-112">Example 2: Create a service in an affinity group</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

<span data-ttu-id="d5e5e-113">Bu komut, kuzeydoğu adlı yeni bir hizmeti MySvc01 adında, kuzeydoğu benzeşim grubunu kullanarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-113">This command creates a new service named MySvc01 using the NorthRegion affinity group.</span></span>

## <span data-ttu-id="d5e5e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5e5e-114">PARAMETERS</span></span>

### <span data-ttu-id="d5e5e-115">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="d5e5e-115">-AffinityGroup</span></span>
<span data-ttu-id="d5e5e-116">Abonelikle ilişkilendirilmiş benzeşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-116">Specifies the affinity group associated with the subscription.</span></span>
<span data-ttu-id="d5e5e-117">*Konum* parametresini belirtmezseniz, bir benzeşim grubu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-117">If you do not specify the *Location* parameter, an affinity group is required.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5e5e-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d5e5e-118">-Description</span></span>
<span data-ttu-id="d5e5e-119">Hizmetin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-119">Specifies a description for the service.</span></span>
<span data-ttu-id="d5e5e-120">Açıklama en çok 1024 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-120">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5e5e-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d5e5e-121">-InformationAction</span></span>
<span data-ttu-id="d5e5e-122">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d5e5e-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d5e5e-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5e5e-124">'A</span><span class="sxs-lookup"><span data-stu-id="d5e5e-124">Continue</span></span>
- <span data-ttu-id="d5e5e-125">Manıza</span><span class="sxs-lookup"><span data-stu-id="d5e5e-125">Ignore</span></span>
- <span data-ttu-id="d5e5e-126">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="d5e5e-126">Inquire</span></span>
- <span data-ttu-id="d5e5e-127">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="d5e5e-127">SilentlyContinue</span></span>
- <span data-ttu-id="d5e5e-128">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="d5e5e-128">Stop</span></span>
- <span data-ttu-id="d5e5e-129">Biliriz</span><span class="sxs-lookup"><span data-stu-id="d5e5e-129">Suspend</span></span>

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

### <span data-ttu-id="d5e5e-130">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="d5e5e-130">-InformationVariable</span></span>
<span data-ttu-id="d5e5e-131">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d5e5e-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d5e5e-132">-Label</span></span>
<span data-ttu-id="d5e5e-133">Hizmetin etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-133">Specifies a label for the service.</span></span>
<span data-ttu-id="d5e5e-134">Etiket en çok 100 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-134">The label may be up to 100 characters in length.</span></span>

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

### <span data-ttu-id="d5e5e-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="d5e5e-135">-Location</span></span>
<span data-ttu-id="d5e5e-136">Hizmetin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-136">Specifies the location for the service.</span></span>
<span data-ttu-id="d5e5e-137">Belirtilen benzeşim grubu olmadığında konum gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-137">A location is required if there isn't a specified Affinity Group.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5e5e-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="d5e5e-138">-Profile</span></span>
<span data-ttu-id="d5e5e-139">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d5e5e-140">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5e5e-141">-Smardnsfqdn</span><span class="sxs-lookup"><span data-stu-id="d5e5e-141">-ReverseDnsFqdn</span></span>
<span data-ttu-id="d5e5e-142">Geriye doğru DNS için tam nitelikli etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-142">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5e5e-143">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="d5e5e-143">-ServiceName</span></span>
<span data-ttu-id="d5e5e-144">Yeni hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-144">Specifies the name of the new service.</span></span>
<span data-ttu-id="d5e5e-145">Ad, aboneliğe özgü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-145">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="d5e5e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e5e-146">CommonParameters</span></span>
<span data-ttu-id="d5e5e-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5e5e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e5e-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5e5e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e5e-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5e5e-149">INPUTS</span></span>

## <span data-ttu-id="d5e5e-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5e5e-150">OUTPUTS</span></span>

## <span data-ttu-id="d5e5e-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5e5e-151">NOTES</span></span>

## <span data-ttu-id="d5e5e-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5e5e-152">RELATED LINKS</span></span>

[<span data-ttu-id="d5e5e-153">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="d5e5e-153">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="d5e5e-154">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="d5e5e-154">Set-AzureService</span></span>](./Set-AzureService.md)


