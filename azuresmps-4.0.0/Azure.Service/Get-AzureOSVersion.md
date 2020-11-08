---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105637"
---
# <span data-ttu-id="06776-101">Get-AzureOSVersion</span><span class="sxs-lookup"><span data-stu-id="06776-101">Get-AzureOSVersion</span></span>

## <span data-ttu-id="06776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06776-102">SYNOPSIS</span></span>
<span data-ttu-id="06776-103">Tüm Azure Konuk işletim sistemlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="06776-103">Lists all Azure guest operating systems.</span></span>

## <span data-ttu-id="06776-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06776-104">SYNTAX</span></span>

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="06776-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06776-105">DESCRIPTION</span></span>
<span data-ttu-id="06776-106">**Get-AzureOSVersion** cmdlet 'i kullanılabilir tüm Azure Konuk işletim sistemlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="06776-106">The **Get-AzureOSVersion** cmdlet lists all the available Azure guest operating systems.</span></span>

## <span data-ttu-id="06776-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06776-107">EXAMPLES</span></span>

### <span data-ttu-id="06776-108">Örnek 1: tüm kullanılabilir işletim sistemlerini edinme</span><span class="sxs-lookup"><span data-stu-id="06776-108">Example 1: Get all available operating systems</span></span>
```
PS C:\> Get-AzureOSVersion
```

<span data-ttu-id="06776-109">Bu komut, geçerli abonelikteki tüm konuk işletim sistemi sürümlerinin listesini içeren bir nesne alır.</span><span class="sxs-lookup"><span data-stu-id="06776-109">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>

### <span data-ttu-id="06776-110">Örnek 2: bir tabloda işletim sistemi bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="06776-110">Example 2: Display operating system information in a table</span></span>
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

<span data-ttu-id="06776-111">Bu komut, geçerli abonelikteki tüm konuk işletim sistemi sürümlerinin listesini içeren bir nesne alır.</span><span class="sxs-lookup"><span data-stu-id="06776-111">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>
<span data-ttu-id="06776-112">Komut, ardışık düzen işlecini kullanarak bunları **Biçim-Tablo** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="06776-112">The command passes them to the **Format-Table** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="06776-113">Bu cmdlet, bunları işletim sistemi ailesini, işletim sistemi aile etiketini ve sürümü gösteren bir tablo olarak biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="06776-113">That cmdlet formats them as a table that shows the operating system family, operating system family label, and version.</span></span>

## <span data-ttu-id="06776-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06776-114">PARAMETERS</span></span>

### <span data-ttu-id="06776-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="06776-115">-InformationAction</span></span>
<span data-ttu-id="06776-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06776-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="06776-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="06776-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06776-118">'A</span><span class="sxs-lookup"><span data-stu-id="06776-118">Continue</span></span>
- <span data-ttu-id="06776-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="06776-119">Ignore</span></span>
- <span data-ttu-id="06776-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="06776-120">Inquire</span></span>
- <span data-ttu-id="06776-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="06776-121">SilentlyContinue</span></span>
- <span data-ttu-id="06776-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="06776-122">Stop</span></span>
- <span data-ttu-id="06776-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="06776-123">Suspend</span></span>

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

### <span data-ttu-id="06776-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="06776-124">-InformationVariable</span></span>
<span data-ttu-id="06776-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="06776-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="06776-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="06776-126">-Profile</span></span>
<span data-ttu-id="06776-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06776-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06776-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="06776-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06776-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06776-129">CommonParameters</span></span>
<span data-ttu-id="06776-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06776-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06776-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06776-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06776-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06776-132">INPUTS</span></span>

## <span data-ttu-id="06776-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06776-133">OUTPUTS</span></span>

## <span data-ttu-id="06776-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06776-134">NOTES</span></span>

## <span data-ttu-id="06776-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06776-135">RELATED LINKS</span></span>

[<span data-ttu-id="06776-136">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="06776-136">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)


