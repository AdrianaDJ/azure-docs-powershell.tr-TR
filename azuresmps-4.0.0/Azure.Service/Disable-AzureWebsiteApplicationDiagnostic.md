---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3422EFD0-88DC-4DF0-868C-5C63C9FA95EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9aa78f34abf17c2aa5858697f492f76ee124d91
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105690"
---
# <span data-ttu-id="3ef10-101">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3ef10-101">Disable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="3ef10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ef10-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef10-103">Azure Web sitesi için uygulama tanılamayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3ef10-103">Disables application diagnostics for an Azure website.</span></span>

## <span data-ttu-id="3ef10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ef10-104">SYNTAX</span></span>

```
Disable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] [-TableStorage] [-BlobStorage] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3ef10-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ef10-105">DESCRIPTION</span></span>
<span data-ttu-id="3ef10-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3ef10-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3ef10-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3ef10-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3ef10-108">Azure Web sitesi için uygulama tanılamayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3ef10-108">Disables application diagnostics for an Azure website.</span></span>
<span data-ttu-id="3ef10-109">Bir dosya sisteminde veya Azure 'da depolanması için yapılandırılmış günlüğü devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3ef10-109">Disables logging configured to be stored on a file system or on Azure.</span></span>

## <span data-ttu-id="3ef10-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ef10-110">EXAMPLES</span></span>

### <span data-ttu-id="3ef10-111">Örnek 1: uygulama günlüğü dosyasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="3ef10-111">Example 1:  Disable application logging file</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File
```

<span data-ttu-id="3ef10-112">Aşağıdaki örnek, dosya sisteminde uygulama günlüğünü devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3ef10-112">The following example disables application logging on the file system.</span></span>

### <span data-ttu-id="3ef10-113">Örnek 2: Azure depolama kullanarak günlüğü devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="3ef10-113">Example 2:  Disable logging using Azure storage</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage
```

<span data-ttu-id="3ef10-114">Aşağıdaki örnek, depolama kullanarak uygulama günlüğünü devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="3ef10-114">The following example disables application logging using storage.</span></span>

## <span data-ttu-id="3ef10-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ef10-115">PARAMETERS</span></span>

### <span data-ttu-id="3ef10-116">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="3ef10-116">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef10-117">-Dosya</span><span class="sxs-lookup"><span data-stu-id="3ef10-117">-File</span></span>
<span data-ttu-id="3ef10-118">Günlük dosyalarını depolamak için dosya sistemini kullanmak istediğinizi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef10-118">Specifies that you want to use the file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef10-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ef10-119">-Name</span></span>
<span data-ttu-id="3ef10-120">Web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef10-120">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="3ef10-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3ef10-121">-PassThru</span></span>
<span data-ttu-id="3ef10-122">Doğru değerini döndürmek için bayrak.</span><span class="sxs-lookup"><span data-stu-id="3ef10-122">Flag to return true if succeeded.</span></span>

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

### <span data-ttu-id="3ef10-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="3ef10-123">-Profile</span></span>
<span data-ttu-id="3ef10-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef10-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ef10-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3ef10-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ef10-126">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="3ef10-126">-Slot</span></span>
<span data-ttu-id="3ef10-127">Yuvanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef10-127">Specifies the name of slot.</span></span>

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

### <span data-ttu-id="3ef10-128">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="3ef10-128">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef10-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef10-129">CommonParameters</span></span>
<span data-ttu-id="3ef10-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ef10-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef10-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef10-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef10-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ef10-132">INPUTS</span></span>

## <span data-ttu-id="3ef10-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ef10-133">OUTPUTS</span></span>

## <span data-ttu-id="3ef10-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ef10-134">NOTES</span></span>

## <span data-ttu-id="3ef10-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ef10-135">RELATED LINKS</span></span>

[<span data-ttu-id="3ef10-136">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3ef10-136">Enable-AzureWebsiteApplicationDiagnostic</span></span>](./Enable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="3ef10-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3ef10-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="3ef10-138">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3ef10-138">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="3ef10-139">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3ef10-139">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="3ef10-140">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3ef10-140">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


