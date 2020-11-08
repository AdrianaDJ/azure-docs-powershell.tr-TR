---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 19A87B24-C5A6-4505-BB54-973B24BCC68E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821927fc465ed5af048a2f27ed84da8c12b9caa5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106536"
---
# <span data-ttu-id="d6af5-101">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="d6af5-101">Get-AzureVMDscExtensionStatus</span></span>

## <span data-ttu-id="d6af5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6af5-102">SYNOPSIS</span></span>
<span data-ttu-id="d6af5-103">Bir bulut hizmetinde dağıtılan tüm sanal makinelerin veya hizmette belirli bir sanal makinenin DSC Uzantısı durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="d6af5-103">Gets the DSC extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="d6af5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6af5-104">SYNTAX</span></span>

### <span data-ttu-id="d6af5-105">GetStatusByServiceAndVMName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d6af5-105">GetStatusByServiceAndVMName (Default)</span></span>
```
Get-AzureVMDscExtensionStatus [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d6af5-106">GetStatusByVM</span><span class="sxs-lookup"><span data-stu-id="d6af5-106">GetStatusByVM</span></span>
```
Get-AzureVMDscExtensionStatus -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d6af5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6af5-107">DESCRIPTION</span></span>
<span data-ttu-id="d6af5-108">**Get-AzureVMDscExtensionStatus** cmdlet 'i, bir bulut hizmetinde dağıtılan tüm sanal makinelerin veya hizmette belirli bir sanal makinenin Istenen durum YAPıLANDıRMASı (DSC) uzantı durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="d6af5-108">The **Get-AzureVMDscExtensionStatus** cmdlet gets the Desired State Configuration (DSC) extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="d6af5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6af5-109">EXAMPLES</span></span>

### <span data-ttu-id="d6af5-110">2</span><span class="sxs-lookup"><span data-stu-id="d6af5-110">1:</span></span>
```

```

## <span data-ttu-id="d6af5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6af5-111">PARAMETERS</span></span>

### <span data-ttu-id="d6af5-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d6af5-112">-InformationAction</span></span>
<span data-ttu-id="d6af5-113">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6af5-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d6af5-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d6af5-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6af5-115">'A</span><span class="sxs-lookup"><span data-stu-id="d6af5-115">Continue</span></span>
- <span data-ttu-id="d6af5-116">Manıza</span><span class="sxs-lookup"><span data-stu-id="d6af5-116">Ignore</span></span>
- <span data-ttu-id="d6af5-117">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="d6af5-117">Inquire</span></span>
- <span data-ttu-id="d6af5-118">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="d6af5-118">SilentlyContinue</span></span>
- <span data-ttu-id="d6af5-119">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="d6af5-119">Stop</span></span>
- <span data-ttu-id="d6af5-120">Biliriz</span><span class="sxs-lookup"><span data-stu-id="d6af5-120">Suspend</span></span>

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

### <span data-ttu-id="d6af5-121">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="d6af5-121">-InformationVariable</span></span>
<span data-ttu-id="d6af5-122">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6af5-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d6af5-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d6af5-123">-Name</span></span>
<span data-ttu-id="d6af5-124">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6af5-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af5-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="d6af5-125">-Profile</span></span>
<span data-ttu-id="d6af5-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6af5-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6af5-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d6af5-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6af5-128">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="d6af5-128">-ServiceName</span></span>
<span data-ttu-id="d6af5-129">Hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6af5-129">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af5-130">-VM</span><span class="sxs-lookup"><span data-stu-id="d6af5-130">-VM</span></span>
<span data-ttu-id="d6af5-131">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6af5-131">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: GetStatusByVM
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6af5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6af5-132">CommonParameters</span></span>
<span data-ttu-id="d6af5-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6af5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6af5-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6af5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6af5-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6af5-135">INPUTS</span></span>

## <span data-ttu-id="d6af5-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6af5-136">OUTPUTS</span></span>

### <span data-ttu-id="d6af5-137">Microsoft. Windowsazde. Commands. ServiceManagement. IaaS. Extensions. VirtualMachineDscExtensionStatusContext</span><span class="sxs-lookup"><span data-stu-id="d6af5-137">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionStatusContext</span></span>

## <span data-ttu-id="d6af5-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6af5-138">NOTES</span></span>

## <span data-ttu-id="d6af5-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6af5-139">RELATED LINKS</span></span>

[<span data-ttu-id="d6af5-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d6af5-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="d6af5-141">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d6af5-141">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="d6af5-142">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d6af5-142">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


