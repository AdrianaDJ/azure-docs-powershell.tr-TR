---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2dca85290564217f5c4c319ef3531d4c31500fcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106584"
---
# <span data-ttu-id="e098f-101">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="e098f-101">Get-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="e098f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e098f-102">SYNOPSIS</span></span>

## <span data-ttu-id="e098f-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e098f-103">SYNTAX</span></span>

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e098f-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="e098f-104">DESCRIPTION</span></span>

## <span data-ttu-id="e098f-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e098f-105">EXAMPLES</span></span>

### <span data-ttu-id="e098f-106">2</span><span class="sxs-lookup"><span data-stu-id="e098f-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e098f-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e098f-107">PARAMETERS</span></span>

### <span data-ttu-id="e098f-108">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e098f-108">-InformationAction</span></span>
<span data-ttu-id="e098f-109">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e098f-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e098f-110">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e098f-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e098f-111">'A</span><span class="sxs-lookup"><span data-stu-id="e098f-111">Continue</span></span>
- <span data-ttu-id="e098f-112">Manıza</span><span class="sxs-lookup"><span data-stu-id="e098f-112">Ignore</span></span>
- <span data-ttu-id="e098f-113">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="e098f-113">Inquire</span></span>
- <span data-ttu-id="e098f-114">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="e098f-114">SilentlyContinue</span></span>
- <span data-ttu-id="e098f-115">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="e098f-115">Stop</span></span>
- <span data-ttu-id="e098f-116">Biliriz</span><span class="sxs-lookup"><span data-stu-id="e098f-116">Suspend</span></span>

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

### <span data-ttu-id="e098f-117">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="e098f-117">-InformationVariable</span></span>
<span data-ttu-id="e098f-118">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="e098f-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e098f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e098f-119">-Name</span></span>
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

### <span data-ttu-id="e098f-120">-VM</span><span class="sxs-lookup"><span data-stu-id="e098f-120">-VM</span></span>
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e098f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e098f-121">CommonParameters</span></span>
<span data-ttu-id="e098f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e098f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e098f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e098f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e098f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e098f-124">INPUTS</span></span>

## <span data-ttu-id="e098f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e098f-125">OUTPUTS</span></span>

## <span data-ttu-id="e098f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e098f-126">NOTES</span></span>

## <span data-ttu-id="e098f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e098f-127">RELATED LINKS</span></span>

[<span data-ttu-id="e098f-128">Add-Azurenetworkınterfaceconfig</span><span class="sxs-lookup"><span data-stu-id="e098f-128">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="e098f-129">Remove-Azurenetworkınterfaceconfig</span><span class="sxs-lookup"><span data-stu-id="e098f-129">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="e098f-130">Set-Azurenetworkınterfaceconfig</span><span class="sxs-lookup"><span data-stu-id="e098f-130">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


