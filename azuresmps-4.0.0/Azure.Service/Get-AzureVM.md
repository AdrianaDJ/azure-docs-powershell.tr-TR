---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106547"
---
# <span data-ttu-id="af65c-101">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="af65c-101">Get-AzureVM</span></span>

## <span data-ttu-id="af65c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af65c-102">SYNOPSIS</span></span>
<span data-ttu-id="af65c-103">Bir veya daha fazla Azure sanal makinelerinden bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="af65c-103">Retrieves information from one or more Azure virtual machines.</span></span>

## <span data-ttu-id="af65c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af65c-104">SYNTAX</span></span>

### <span data-ttu-id="af65c-105">ListAllVMs (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af65c-105">ListAllVMs (Default)</span></span>
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="af65c-106">GetVMByServiceAndVMName</span><span class="sxs-lookup"><span data-stu-id="af65c-106">GetVMByServiceAndVMName</span></span>
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="af65c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af65c-107">DESCRIPTION</span></span>
<span data-ttu-id="af65c-108">**Get-AzureVM** cmdlet 'i Azure 'da çalışan sanal makineler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="af65c-108">The **Get-AzureVM** cmdlet retrieves information about virtual machines running in Azure.</span></span>
<span data-ttu-id="af65c-109">Belirli bir sanal makinede bilgi içeren bir nesne veya geçerli aboneliğin belirtilen hizmetindeki tüm sanal makineler için sanal makine belirtilmemişse bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="af65c-109">It returns an object with information on a specific virtual machine, or if no virtual machine is specified, for all the virtual machines in the specified service of the current subscription.</span></span>

## <span data-ttu-id="af65c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af65c-110">EXAMPLES</span></span>

### <span data-ttu-id="af65c-111">Örnek 1: belirtilen sanal makinedeki bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="af65c-111">Example 1: Retrieve information on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

<span data-ttu-id="af65c-112">Bu komut, ContosoService01 bulut hizmetinde çalışan VirtualMachine02 sanal makinesindeki bilgileri içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="af65c-112">This command returns an object with information on the VirtualMachine02 virtual machine running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="af65c-113">Örnek 2: tüm sanal makinelerde bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="af65c-113">Example 2: Retrieve information on all virtual machines</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

<span data-ttu-id="af65c-114">Bu komut, ContosoService01 bulut hizmetinde çalışan tüm sanal makinelerde bilgi içeren bir liste nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="af65c-114">This command retrieves a list object with information on all of the virtual machines running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="af65c-115">Örnek 3: sanal makine durumlarının tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="af65c-115">Example 3: Display a table of virtual machine statuses</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

<span data-ttu-id="af65c-116">Bu komut, ContosoService01 hizmetinde çalışan sanal makinelerin, yükseltme etki alanının ve her sanal makinenin geçerli durumunun gösterildiği bir tablo görüntüler.</span><span class="sxs-lookup"><span data-stu-id="af65c-116">This command displays a table showing the virtual machines running on the ContosoService01 service, their Upgrade Domain, and the current status of each virtual machine.</span></span>

## <span data-ttu-id="af65c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af65c-117">PARAMETERS</span></span>

### <span data-ttu-id="af65c-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="af65c-118">-InformationAction</span></span>
<span data-ttu-id="af65c-119">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af65c-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="af65c-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af65c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="af65c-121">'A</span><span class="sxs-lookup"><span data-stu-id="af65c-121">Continue</span></span>
- <span data-ttu-id="af65c-122">Manıza</span><span class="sxs-lookup"><span data-stu-id="af65c-122">Ignore</span></span>
- <span data-ttu-id="af65c-123">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="af65c-123">Inquire</span></span>
- <span data-ttu-id="af65c-124">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="af65c-124">SilentlyContinue</span></span>
- <span data-ttu-id="af65c-125">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="af65c-125">Stop</span></span>
- <span data-ttu-id="af65c-126">Biliriz</span><span class="sxs-lookup"><span data-stu-id="af65c-126">Suspend</span></span>

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

### <span data-ttu-id="af65c-127">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="af65c-127">-InformationVariable</span></span>
<span data-ttu-id="af65c-128">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="af65c-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="af65c-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="af65c-129">-Name</span></span>
<span data-ttu-id="af65c-130">Bilgileri alacak sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af65c-130">Specifies the name of the virtual machine for which to retrieve information.</span></span>
<span data-ttu-id="af65c-131">Bu parametre sağlanmadıysa cmdlet, belirtilen hizmette tüm sanal makinelerle ilgili bilgileri içeren bir liste nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="af65c-131">If this parameter is not provided, the cmdlet returns a list object with information about all the virtual machines in the specified service.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af65c-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="af65c-132">-Profile</span></span>
<span data-ttu-id="af65c-133">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af65c-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af65c-134">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="af65c-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="af65c-135">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="af65c-135">-ServiceName</span></span>
<span data-ttu-id="af65c-136">Sanal makine bilgileri döndürülecek bulut hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af65c-136">Specifies the name of the cloud service for which to return virtual machine information.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af65c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af65c-137">CommonParameters</span></span>
<span data-ttu-id="af65c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af65c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af65c-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af65c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af65c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af65c-140">INPUTS</span></span>

## <span data-ttu-id="af65c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af65c-141">OUTPUTS</span></span>

## <span data-ttu-id="af65c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af65c-142">NOTES</span></span>

## <span data-ttu-id="af65c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af65c-143">RELATED LINKS</span></span>

[<span data-ttu-id="af65c-144">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="af65c-144">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="af65c-145">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="af65c-145">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="af65c-146">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="af65c-146">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="af65c-147">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="af65c-147">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="af65c-148">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="af65c-148">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="af65c-149">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="af65c-149">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="af65c-150">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="af65c-150">Update-AzureVM</span></span>](./Update-AzureVM.md)


