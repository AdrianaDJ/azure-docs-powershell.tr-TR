---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106431"
---
# <span data-ttu-id="9dce6-101">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="9dce6-101">Set-AzureAffinityGroup</span></span>

## <span data-ttu-id="9dce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dce6-102">SYNOPSIS</span></span>
<span data-ttu-id="9dce6-103">Benzeşim grubunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-103">Modifies properties of an affinity group.</span></span>

## <span data-ttu-id="9dce6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9dce6-104">SYNTAX</span></span>

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9dce6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9dce6-105">DESCRIPTION</span></span>
<span data-ttu-id="9dce6-106">**Set-AzureAffinityGroup** cmdlet 'ı bir Azure benzeşim grubunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-106">The **Set-AzureAffinityGroup** cmdlet modifies properties of an Azure affinity group.</span></span>
<span data-ttu-id="9dce6-107">Etiketi ve açıklamayı değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9dce6-107">You can change the label and the description.</span></span>

## <span data-ttu-id="9dce6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9dce6-108">EXAMPLES</span></span>

### <span data-ttu-id="9dce6-109">Örnek 1: benzeşim grubunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="9dce6-109">Example 1: Modify an affinity group</span></span>
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

<span data-ttu-id="9dce6-110">Bu komut, South01 adlı benzeşim grubunun, Güneydoğu üretim olacak şekilde değiştirir komut ayrıca açıklamayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-110">This command modifies the label of the affinity group named South01 to be SouthUSProduction The command also modifies the description.</span></span>

## <span data-ttu-id="9dce6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9dce6-111">PARAMETERS</span></span>

### <span data-ttu-id="9dce6-112">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9dce6-112">-Description</span></span>
<span data-ttu-id="9dce6-113">Benzeşim grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-113">Specifies the description of the affinity group.</span></span>
<span data-ttu-id="9dce6-114">Açıklama 1024 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-114">The description can be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="9dce6-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9dce6-115">-InformationAction</span></span>
<span data-ttu-id="9dce6-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9dce6-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9dce6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9dce6-118">'A</span><span class="sxs-lookup"><span data-stu-id="9dce6-118">Continue</span></span>
- <span data-ttu-id="9dce6-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="9dce6-119">Ignore</span></span>
- <span data-ttu-id="9dce6-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="9dce6-120">Inquire</span></span>
- <span data-ttu-id="9dce6-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="9dce6-121">SilentlyContinue</span></span>
- <span data-ttu-id="9dce6-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="9dce6-122">Stop</span></span>
- <span data-ttu-id="9dce6-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="9dce6-123">Suspend</span></span>

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

### <span data-ttu-id="9dce6-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="9dce6-124">-InformationVariable</span></span>
<span data-ttu-id="9dce6-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9dce6-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9dce6-126">-Label</span></span>
<span data-ttu-id="9dce6-127">Benzeşim grubu için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-127">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="9dce6-128">Etiket en çok 100 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-128">The label can be up to 100 characters long.</span></span>

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

### <span data-ttu-id="9dce6-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="9dce6-129">-Name</span></span>
<span data-ttu-id="9dce6-130">Bu cmdlet 'in değiştirdiği benzeşim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-130">Specifies the name of the affinity group that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9dce6-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="9dce6-131">-Profile</span></span>
<span data-ttu-id="9dce6-132">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dce6-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9dce6-133">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9dce6-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9dce6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dce6-134">CommonParameters</span></span>
<span data-ttu-id="9dce6-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9dce6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dce6-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dce6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dce6-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9dce6-137">INPUTS</span></span>

## <span data-ttu-id="9dce6-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9dce6-138">OUTPUTS</span></span>

## <span data-ttu-id="9dce6-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9dce6-139">NOTES</span></span>

## <span data-ttu-id="9dce6-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9dce6-140">RELATED LINKS</span></span>

[<span data-ttu-id="9dce6-141">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="9dce6-141">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="9dce6-142">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="9dce6-142">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="9dce6-143">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="9dce6-143">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)


