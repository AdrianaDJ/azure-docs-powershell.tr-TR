---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106031"
---
# <span data-ttu-id="1099f-101">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="1099f-101">Start-AzureEmulator</span></span>

## <span data-ttu-id="1099f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1099f-102">SYNOPSIS</span></span>
<span data-ttu-id="1099f-103">Hesaplama ve depolama öykünücüsünü başlatır.</span><span class="sxs-lookup"><span data-stu-id="1099f-103">Starts the compute and storage emulators.</span></span>

## <span data-ttu-id="1099f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1099f-104">SYNTAX</span></span>

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1099f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1099f-105">DESCRIPTION</span></span>
<span data-ttu-id="1099f-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1099f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1099f-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1099f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1099f-108">**Start-AzureEmulator** cmdlet 'i hem COMPUTE hem de depolama öykünücüsünü başlatır ve işlem öykünücüsünde geçerli hizmeti barındırır.</span><span class="sxs-lookup"><span data-stu-id="1099f-108">The **Start-AzureEmulator** cmdlet starts both the compute and storage emulators and hosts the current service in the compute emulator.</span></span>

## <span data-ttu-id="1099f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1099f-109">EXAMPLES</span></span>

### <span data-ttu-id="1099f-110">Örnek 1: öykünücüyü başlatma ve Tarayıcıyı başlatma</span><span class="sxs-lookup"><span data-stu-id="1099f-110">Example 1: Start the emulator and launch a browser</span></span>
```
PS C:\> Start-AzureEmulator -L
```

<span data-ttu-id="1099f-111">Bu örnek, hizmeti Azure öykünücüsü 'nde çalıştırır ve öykünülmüş hizmette yeni bir tarayıcı penceresi başlatır.</span><span class="sxs-lookup"><span data-stu-id="1099f-111">This example runs the service in the Azure emulator and launches a new browser window on the emulated service.</span></span>

## <span data-ttu-id="1099f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1099f-112">PARAMETERS</span></span>

### <span data-ttu-id="1099f-113">-Başlat</span><span class="sxs-lookup"><span data-stu-id="1099f-113">-Launch</span></span>
<span data-ttu-id="1099f-114">Hizmette barındırdıktan sonra hizmette yeni bir tarayıcı penceresi açar.</span><span class="sxs-lookup"><span data-stu-id="1099f-114">Opens a new browser window on the service after hosting it in the emulator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1099f-115">-Mod</span><span class="sxs-lookup"><span data-stu-id="1099f-115">-Mode</span></span>
<span data-ttu-id="1099f-116">Öykünücü modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1099f-116">Specifies the emulator mode.</span></span>
<span data-ttu-id="1099f-117">Geçerli değerler: Full ve Express.</span><span class="sxs-lookup"><span data-stu-id="1099f-117">Valid values are: Full and Express.</span></span>
<span data-ttu-id="1099f-118">Varsayılan değer,</span><span class="sxs-lookup"><span data-stu-id="1099f-118">The default value is Express.</span></span>

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1099f-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="1099f-119">-Profile</span></span>
<span data-ttu-id="1099f-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1099f-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1099f-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1099f-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1099f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1099f-122">CommonParameters</span></span>
<span data-ttu-id="1099f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1099f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1099f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1099f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1099f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1099f-125">INPUTS</span></span>

## <span data-ttu-id="1099f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1099f-126">OUTPUTS</span></span>

## <span data-ttu-id="1099f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1099f-127">NOTES</span></span>

## <span data-ttu-id="1099f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1099f-128">RELATED LINKS</span></span>

[<span data-ttu-id="1099f-129">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="1099f-129">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="1099f-130">Yayımla-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="1099f-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="1099f-131">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="1099f-131">Stop-AzureEmulator</span></span>](./Stop-AzureEmulator.md)


