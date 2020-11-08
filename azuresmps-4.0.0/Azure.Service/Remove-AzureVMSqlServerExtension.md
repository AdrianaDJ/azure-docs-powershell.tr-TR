---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C19A1DC0-47FA-4687-B81F-315EA04AD4A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22591c1aa5a670e8f0d73f206ed6d2bcbe52c88f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105494"
---
# <span data-ttu-id="3c898-101">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3c898-101">Remove-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="3c898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c898-102">SYNOPSIS</span></span>
<span data-ttu-id="3c898-103">Bir sanal makine nesnesinden Azure sanal makine SQL Server uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c898-103">Removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="3c898-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c898-104">SYNTAX</span></span>

```
Remove-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3c898-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c898-105">DESCRIPTION</span></span>
<span data-ttu-id="3c898-106">**Remove-AzureVMSqlServerExtension** cmdlet 'i, bir Azure sanal makine SQL Server uzantısını bir sanal makine nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c898-106">The **Remove-AzureVMSqlServerExtension** cmdlet removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="3c898-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c898-107">EXAMPLES</span></span>

### <span data-ttu-id="3c898-108">2</span><span class="sxs-lookup"><span data-stu-id="3c898-108">1:</span></span>
```

```

## <span data-ttu-id="3c898-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c898-109">PARAMETERS</span></span>

### <span data-ttu-id="3c898-110">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="3c898-110">-InformationAction</span></span>
<span data-ttu-id="3c898-111">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c898-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3c898-112">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3c898-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c898-113">'A</span><span class="sxs-lookup"><span data-stu-id="3c898-113">Continue</span></span>
- <span data-ttu-id="3c898-114">Manıza</span><span class="sxs-lookup"><span data-stu-id="3c898-114">Ignore</span></span>
- <span data-ttu-id="3c898-115">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="3c898-115">Inquire</span></span>
- <span data-ttu-id="3c898-116">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="3c898-116">SilentlyContinue</span></span>
- <span data-ttu-id="3c898-117">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="3c898-117">Stop</span></span>
- <span data-ttu-id="3c898-118">Biliriz</span><span class="sxs-lookup"><span data-stu-id="3c898-118">Suspend</span></span>

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

### <span data-ttu-id="3c898-119">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="3c898-119">-InformationVariable</span></span>
<span data-ttu-id="3c898-120">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c898-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3c898-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c898-121">-Profile</span></span>
<span data-ttu-id="3c898-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c898-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c898-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3c898-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c898-124">-VM</span><span class="sxs-lookup"><span data-stu-id="3c898-124">-VM</span></span>
<span data-ttu-id="3c898-125">Bu cmdlet 'in uzantıyı kaldırdığı kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c898-125">Specifies the persistent virtual machine object that this cmdlet removes the extension from.</span></span>

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

### <span data-ttu-id="3c898-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c898-126">CommonParameters</span></span>
<span data-ttu-id="3c898-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c898-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c898-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c898-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c898-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c898-129">INPUTS</span></span>

## <span data-ttu-id="3c898-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c898-130">OUTPUTS</span></span>

## <span data-ttu-id="3c898-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c898-131">NOTES</span></span>

## <span data-ttu-id="3c898-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c898-132">RELATED LINKS</span></span>

[<span data-ttu-id="3c898-133">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3c898-133">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="3c898-134">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3c898-134">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


