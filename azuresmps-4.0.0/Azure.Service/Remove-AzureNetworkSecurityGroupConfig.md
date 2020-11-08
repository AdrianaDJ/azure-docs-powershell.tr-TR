---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AB4700D-571B-497A-9742-2654844553B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: b46f15053639ec295d958766dac846d4f95e0368
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106151"
---
# <span data-ttu-id="aba16-101">Remove-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="aba16-101">Remove-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="aba16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aba16-102">SYNOPSIS</span></span>

## <span data-ttu-id="aba16-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aba16-103">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupConfig [[-NetworkSecurityGroupName] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="aba16-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="aba16-104">DESCRIPTION</span></span>

## <span data-ttu-id="aba16-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aba16-105">EXAMPLES</span></span>

### <span data-ttu-id="aba16-106">2</span><span class="sxs-lookup"><span data-stu-id="aba16-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="aba16-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aba16-107">PARAMETERS</span></span>

### <span data-ttu-id="aba16-108">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="aba16-108">-InformationAction</span></span>
<span data-ttu-id="aba16-109">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aba16-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aba16-110">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aba16-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aba16-111">'A</span><span class="sxs-lookup"><span data-stu-id="aba16-111">Continue</span></span>
- <span data-ttu-id="aba16-112">Manıza</span><span class="sxs-lookup"><span data-stu-id="aba16-112">Ignore</span></span>
- <span data-ttu-id="aba16-113">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="aba16-113">Inquire</span></span>
- <span data-ttu-id="aba16-114">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="aba16-114">SilentlyContinue</span></span>
- <span data-ttu-id="aba16-115">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="aba16-115">Stop</span></span>
- <span data-ttu-id="aba16-116">Biliriz</span><span class="sxs-lookup"><span data-stu-id="aba16-116">Suspend</span></span>

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

### <span data-ttu-id="aba16-117">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="aba16-117">-InformationVariable</span></span>
<span data-ttu-id="aba16-118">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="aba16-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aba16-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="aba16-119">-NetworkSecurityGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba16-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="aba16-120">-Profile</span></span>
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

### <span data-ttu-id="aba16-121">-VM</span><span class="sxs-lookup"><span data-stu-id="aba16-121">-VM</span></span>
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

### <span data-ttu-id="aba16-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba16-122">CommonParameters</span></span>
<span data-ttu-id="aba16-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aba16-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba16-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba16-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba16-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aba16-125">INPUTS</span></span>

## <span data-ttu-id="aba16-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aba16-126">OUTPUTS</span></span>

## <span data-ttu-id="aba16-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aba16-127">NOTES</span></span>

## <span data-ttu-id="aba16-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aba16-128">RELATED LINKS</span></span>

[<span data-ttu-id="aba16-129">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="aba16-129">Set-AzureNetworkSecurityGroupConfig</span></span>](./Set-AzureNetworkSecurityGroupConfig.md)


