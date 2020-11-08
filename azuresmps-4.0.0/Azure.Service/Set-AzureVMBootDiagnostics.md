---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 846B9EB8-8EC2-4BDA-90EF-59098696F460
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c4e1dedb02286ceaab182e0912198c23ec03ee5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105793"
---
# <span data-ttu-id="2ff2d-101">Set-AzureVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2ff2d-101">Set-AzureVMBootDiagnostics</span></span>

## <span data-ttu-id="2ff2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ff2d-102">SYNOPSIS</span></span>

## <span data-ttu-id="2ff2d-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ff2d-103">SYNTAX</span></span>

### <span data-ttu-id="2ff2d-104">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2ff2d-104">EnableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Enable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2ff2d-105">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2ff2d-105">DisableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2ff2d-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ff2d-106">DESCRIPTION</span></span>

## <span data-ttu-id="2ff2d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ff2d-107">EXAMPLES</span></span>

### <span data-ttu-id="2ff2d-108">2</span><span class="sxs-lookup"><span data-stu-id="2ff2d-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2ff2d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ff2d-109">PARAMETERS</span></span>

### <span data-ttu-id="2ff2d-110">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="2ff2d-110">-Disable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="2ff2d-111">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2ff2d-112">-InformationAction</span></span>
<span data-ttu-id="2ff2d-113">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2ff2d-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2ff2d-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ff2d-115">'A</span><span class="sxs-lookup"><span data-stu-id="2ff2d-115">Continue</span></span>
- <span data-ttu-id="2ff2d-116">Manıza</span><span class="sxs-lookup"><span data-stu-id="2ff2d-116">Ignore</span></span>
- <span data-ttu-id="2ff2d-117">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="2ff2d-117">Inquire</span></span>
- <span data-ttu-id="2ff2d-118">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="2ff2d-118">SilentlyContinue</span></span>
- <span data-ttu-id="2ff2d-119">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="2ff2d-119">Stop</span></span>
- <span data-ttu-id="2ff2d-120">Biliriz</span><span class="sxs-lookup"><span data-stu-id="2ff2d-120">Suspend</span></span>

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

### <span data-ttu-id="2ff2d-121">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="2ff2d-121">-InformationVariable</span></span>
<span data-ttu-id="2ff2d-122">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2ff2d-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="2ff2d-123">-Profile</span></span>
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

### <span data-ttu-id="2ff2d-124">-VM</span><span class="sxs-lookup"><span data-stu-id="2ff2d-124">-VM</span></span>
```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff2d-125">CommonParameters</span></span>
<span data-ttu-id="2ff2d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff2d-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff2d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff2d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ff2d-128">INPUTS</span></span>

## <span data-ttu-id="2ff2d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ff2d-129">OUTPUTS</span></span>

## <span data-ttu-id="2ff2d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ff2d-130">NOTES</span></span>

## <span data-ttu-id="2ff2d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ff2d-131">RELATED LINKS</span></span>

