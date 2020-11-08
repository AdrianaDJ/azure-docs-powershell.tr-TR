---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 455DB2C0-08A0-4D62-B8EE-7C3DB9AD8A8C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85040f07914aef02355f69baab093c75ce7e4afd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105516"
---
# <span data-ttu-id="e40ef-101">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e40ef-101">Remove-AzureVM</span></span>

## <span data-ttu-id="e40ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e40ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e40ef-103">Azure sanal makinesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e40ef-103">Removes an Azure virtual machine.</span></span>

## <span data-ttu-id="e40ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e40ef-104">SYNTAX</span></span>

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e40ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e40ef-105">DESCRIPTION</span></span>
<span data-ttu-id="e40ef-106">**Remove-AzureVM** cmdlet 'ı bir Azure sanal makinesini siler.</span><span class="sxs-lookup"><span data-stu-id="e40ef-106">The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.</span></span>
<span data-ttu-id="e40ef-107">Bu işlem, bu sanal makineye bağlı disklerin temeldeki. vhd dosyalarını silmez.</span><span class="sxs-lookup"><span data-stu-id="e40ef-107">This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.</span></span>

## <span data-ttu-id="e40ef-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e40ef-108">EXAMPLES</span></span>

### <span data-ttu-id="e40ef-109">Örnek 1: hizmetten sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="e40ef-109">Example 1: Remove a virtual machine from a service</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

<span data-ttu-id="e40ef-110">Bu komut, ContosoService03 hizmetinde çalışan VirtualMachine03 adındaki sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e40ef-110">This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.</span></span>

### <span data-ttu-id="e40ef-111">Örnek 2: sanal makineyi kaldırma ve. vhd dosyalarını silme</span><span class="sxs-lookup"><span data-stu-id="e40ef-111">Example 2: Remove a virtual machine and delete the .vhd files</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

<span data-ttu-id="e40ef-112">Bu komut, ContosoService03 hizmetinde çalışan VirtualMachine04 sanal makinesini kaldırır ve *Deletevhd* parametresini kullanarak. vhd dosyalarını kaldırmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e40ef-112">This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="e40ef-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e40ef-113">PARAMETERS</span></span>

### <span data-ttu-id="e40ef-114">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="e40ef-114">-DeleteVHD</span></span>
<span data-ttu-id="e40ef-115">Bu cmdlet 'in sanal makineyi ve temel disk bloblarını kaldırıp kaldırmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e40ef-115">Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e40ef-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e40ef-116">-InformationAction</span></span>
<span data-ttu-id="e40ef-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e40ef-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e40ef-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e40ef-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e40ef-119">'A</span><span class="sxs-lookup"><span data-stu-id="e40ef-119">Continue</span></span>
- <span data-ttu-id="e40ef-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="e40ef-120">Ignore</span></span>
- <span data-ttu-id="e40ef-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="e40ef-121">Inquire</span></span>
- <span data-ttu-id="e40ef-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="e40ef-122">SilentlyContinue</span></span>
- <span data-ttu-id="e40ef-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="e40ef-123">Stop</span></span>
- <span data-ttu-id="e40ef-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="e40ef-124">Suspend</span></span>

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

### <span data-ttu-id="e40ef-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="e40ef-125">-InformationVariable</span></span>
<span data-ttu-id="e40ef-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="e40ef-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e40ef-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="e40ef-127">-Name</span></span>
<span data-ttu-id="e40ef-128">Kaldırılmakta olan sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e40ef-128">Specifies the name of the virtual machine being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e40ef-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="e40ef-129">-Profile</span></span>
<span data-ttu-id="e40ef-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e40ef-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e40ef-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e40ef-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e40ef-132">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="e40ef-132">-ServiceName</span></span>
<span data-ttu-id="e40ef-133">Sanal makinenin kaldırıldığı Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e40ef-133">Specifies the name of the Azure service from which the virtual machine is being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e40ef-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="e40ef-134">-Confirm</span></span>
<span data-ttu-id="e40ef-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e40ef-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e40ef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e40ef-136">-WhatIf</span></span>
<span data-ttu-id="e40ef-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e40ef-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e40ef-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e40ef-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e40ef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e40ef-139">CommonParameters</span></span>
<span data-ttu-id="e40ef-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e40ef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e40ef-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e40ef-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e40ef-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e40ef-142">INPUTS</span></span>

## <span data-ttu-id="e40ef-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e40ef-143">OUTPUTS</span></span>

## <span data-ttu-id="e40ef-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e40ef-144">NOTES</span></span>

## <span data-ttu-id="e40ef-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e40ef-145">RELATED LINKS</span></span>

[<span data-ttu-id="e40ef-146">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e40ef-146">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="e40ef-147">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="e40ef-147">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="e40ef-148">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e40ef-148">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="e40ef-149">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e40ef-149">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="e40ef-150">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e40ef-150">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="e40ef-151">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e40ef-151">Update-AzureVM</span></span>](./Update-AzureVM.md)


