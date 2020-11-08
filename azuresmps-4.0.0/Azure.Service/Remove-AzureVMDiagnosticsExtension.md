---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105504"
---
# <span data-ttu-id="fe9fe-101">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fe9fe-101">Remove-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="fe9fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe9fe-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9fe-103">Sanal makineden Azure tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-103">Removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="fe9fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe9fe-104">SYNTAX</span></span>

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fe9fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe9fe-105">DESCRIPTION</span></span>
<span data-ttu-id="fe9fe-106">**Remove-AzureVMDiagnosticsExtension** cmdlet 'i, bir sanal makineden Microsoft Azure tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-106">The **Remove-AzureVMDiagnosticsExtension** cmdlet removes a Microsoft Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="fe9fe-107">Bu cmdlet 'in çıkışını **Update-AzureVM** cmdlet 'ine geçirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-107">You must pass the output of this cmdlet to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="fe9fe-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe9fe-108">EXAMPLES</span></span>

### <span data-ttu-id="fe9fe-109">Örnek 1: sanal makineden Azure tanılama uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fe9fe-109">Example 1: Remove the Azure Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="fe9fe-110">Bu komut, bir sanal makineden Azure tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-110">This command removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="fe9fe-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe9fe-111">PARAMETERS</span></span>

### <span data-ttu-id="fe9fe-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fe9fe-112">-InformationAction</span></span>
<span data-ttu-id="fe9fe-113">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fe9fe-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fe9fe-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe9fe-115">'A</span><span class="sxs-lookup"><span data-stu-id="fe9fe-115">Continue</span></span>
- <span data-ttu-id="fe9fe-116">Manıza</span><span class="sxs-lookup"><span data-stu-id="fe9fe-116">Ignore</span></span>
- <span data-ttu-id="fe9fe-117">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fe9fe-117">Inquire</span></span>
- <span data-ttu-id="fe9fe-118">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fe9fe-118">SilentlyContinue</span></span>
- <span data-ttu-id="fe9fe-119">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fe9fe-119">Stop</span></span>
- <span data-ttu-id="fe9fe-120">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fe9fe-120">Suspend</span></span>

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

### <span data-ttu-id="fe9fe-121">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fe9fe-121">-InformationVariable</span></span>
<span data-ttu-id="fe9fe-122">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fe9fe-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="fe9fe-123">-Profile</span></span>
<span data-ttu-id="fe9fe-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe9fe-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe9fe-126">-VM</span><span class="sxs-lookup"><span data-stu-id="fe9fe-126">-VM</span></span>
<span data-ttu-id="fe9fe-127">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="fe9fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9fe-128">CommonParameters</span></span>
<span data-ttu-id="fe9fe-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9fe-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe9fe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9fe-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe9fe-131">INPUTS</span></span>

## <span data-ttu-id="fe9fe-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe9fe-132">OUTPUTS</span></span>

## <span data-ttu-id="fe9fe-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe9fe-133">NOTES</span></span>

## <span data-ttu-id="fe9fe-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe9fe-134">RELATED LINKS</span></span>

[<span data-ttu-id="fe9fe-135">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fe9fe-135">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="fe9fe-136">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fe9fe-136">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="fe9fe-137">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fe9fe-137">Update-AzureVM</span></span>](./Update-AzureVM.md)


