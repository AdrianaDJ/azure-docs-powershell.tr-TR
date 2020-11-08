---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 939A28A4-394A-4447-9EFA-8F2876D04DCD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b140c2c0efac81e361e2bab510cfeaf6210ef884
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105807"
---
# <span data-ttu-id="6cd4d-101">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="6cd4d-101">Stop-AzureService</span></span>

## <span data-ttu-id="6cd4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cd4d-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd4d-103">Geçerli barındırılan hizmeti durdurur.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-103">Stops the current hosted service.</span></span>

## <span data-ttu-id="6cd4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6cd4d-104">SYNTAX</span></span>

```
Stop-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cd4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6cd4d-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd4d-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6cd4d-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6cd4d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6cd4d-108">**Stop-AzureService** cmdlet 'ı, Windows Azure 'da Belirtilen yuvadaki geçerli barındırılan hizmeti durdurur.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-108">The **Stop-AzureService** cmdlet stops the current hosted service in the specified slot in Windows Azure.</span></span>
<span data-ttu-id="6cd4d-109">Bir yuva belirtilmemişse, cmdlet üretim yuvasında hizmeti durdurur.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-109">If no slot is specified, the cmdlet stops the service in the Production slot.</span></span>

## <span data-ttu-id="6cd4d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6cd4d-110">EXAMPLES</span></span>

## <span data-ttu-id="6cd4d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6cd4d-111">PARAMETERS</span></span>

### <span data-ttu-id="6cd4d-112">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6cd4d-112">-PassThru</span></span>
<span data-ttu-id="6cd4d-113">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6cd4d-114">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6cd4d-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="6cd4d-115">-Profile</span></span>
<span data-ttu-id="6cd4d-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6cd4d-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6cd4d-118">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="6cd4d-118">-ServiceName</span></span>
<span data-ttu-id="6cd4d-119">Durdurulacak barındırılan hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-119">Specifies the name of the hosted service to stop.</span></span>
<span data-ttu-id="6cd4d-120">Ad belirtilmezse cmdlet, geçerli barındırılan hizmeti durdurur.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-120">If no name is specified, the cmdlet stops the current hosted service.</span></span>

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

### <span data-ttu-id="6cd4d-121">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="6cd4d-121">-Slot</span></span>
<span data-ttu-id="6cd4d-122">Hizmetin barındırıldığı veya üretiminin olduğu yuvayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-122">Specifies the slot where the service is hosted, either Staging or Production.</span></span>
<span data-ttu-id="6cd4d-123">Hiçbir yuva belirtilmemişse, üretim varsayılır.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-123">If no slot is specified,  Production is assumed.</span></span>

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

### <span data-ttu-id="6cd4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd4d-124">CommonParameters</span></span>
<span data-ttu-id="6cd4d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd4d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd4d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd4d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6cd4d-127">INPUTS</span></span>

## <span data-ttu-id="6cd4d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6cd4d-128">OUTPUTS</span></span>

## <span data-ttu-id="6cd4d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6cd4d-129">NOTES</span></span>

## <span data-ttu-id="6cd4d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6cd4d-130">RELATED LINKS</span></span>

[<span data-ttu-id="6cd4d-131">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="6cd4d-131">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="6cd4d-132">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="6cd4d-132">Start-AzureService</span></span>](./Start-AzureService.md)


