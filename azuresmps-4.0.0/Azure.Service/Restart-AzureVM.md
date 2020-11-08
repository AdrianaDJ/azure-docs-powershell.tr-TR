---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 596B8A6F-D3C2-4170-BCD7-B7A1CDB656D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee767e1ba4c5008837e7cef98aafa4017465829
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106073"
---
# <span data-ttu-id="06bf2-101">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06bf2-101">Restart-AzureVM</span></span>

## <span data-ttu-id="06bf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="06bf2-103">Azure sanal makinesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="06bf2-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="06bf2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06bf2-104">SYNTAX</span></span>

### <span data-ttu-id="06bf2-105">RestartByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06bf2-105">RestartByName (Default)</span></span>
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="06bf2-106">RedeployByName</span><span class="sxs-lookup"><span data-stu-id="06bf2-106">RedeployByName</span></span>
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="06bf2-107">InitiateMaintenanceByName</span><span class="sxs-lookup"><span data-stu-id="06bf2-107">InitiateMaintenanceByName</span></span>
```
Restart-AzureVM [-Name] <String> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="06bf2-108">RestartInput</span><span class="sxs-lookup"><span data-stu-id="06bf2-108">RestartInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="06bf2-109">Redeployınput</span><span class="sxs-lookup"><span data-stu-id="06bf2-109">RedeployInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="06bf2-110">InitiateMaintenanceInput</span><span class="sxs-lookup"><span data-stu-id="06bf2-110">InitiateMaintenanceInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="06bf2-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="06bf2-111">DESCRIPTION</span></span>
<span data-ttu-id="06bf2-112">**Restart-AzureVM** cmdlet 'ı bir Azure sanal makinesinin yeniden başlatılmasını ister.</span><span class="sxs-lookup"><span data-stu-id="06bf2-112">The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.</span></span>

## <span data-ttu-id="06bf2-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06bf2-113">EXAMPLES</span></span>

### <span data-ttu-id="06bf2-114">Örnek 1: sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="06bf2-114">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

<span data-ttu-id="06bf2-115">Bu komut, Service01 adındaki Azure hizmetinde çalışan VirtualMachine27 sanal makinesini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="06bf2-115">This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.</span></span>

### <span data-ttu-id="06bf2-116">Örnek 2: sanal makine nesnesini kullanarak sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="06bf2-116">Example 2: Restart a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

<span data-ttu-id="06bf2-117">Bu komut MyVM adındaki sanal makine için sanal makine nesnesini alır ve ardından yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="06bf2-117">This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.</span></span>

## <span data-ttu-id="06bf2-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06bf2-118">PARAMETERS</span></span>

### <span data-ttu-id="06bf2-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="06bf2-119">-InformationAction</span></span>
<span data-ttu-id="06bf2-120">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06bf2-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="06bf2-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="06bf2-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06bf2-122">'A</span><span class="sxs-lookup"><span data-stu-id="06bf2-122">Continue</span></span>
- <span data-ttu-id="06bf2-123">Manıza</span><span class="sxs-lookup"><span data-stu-id="06bf2-123">Ignore</span></span>
- <span data-ttu-id="06bf2-124">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="06bf2-124">Inquire</span></span>
- <span data-ttu-id="06bf2-125">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="06bf2-125">SilentlyContinue</span></span>
- <span data-ttu-id="06bf2-126">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="06bf2-126">Stop</span></span>
- <span data-ttu-id="06bf2-127">Biliriz</span><span class="sxs-lookup"><span data-stu-id="06bf2-127">Suspend</span></span>

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

### <span data-ttu-id="06bf2-128">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="06bf2-128">-InformationVariable</span></span>
<span data-ttu-id="06bf2-129">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="06bf2-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="06bf2-130">-Initiatemaintenance</span><span class="sxs-lookup"><span data-stu-id="06bf2-130">-InitiateMaintenance</span></span>
<span data-ttu-id="06bf2-131">Sanal makinede bakım başlatma</span><span class="sxs-lookup"><span data-stu-id="06bf2-131">Initiate Maintenance on the Virtual Machine</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: InitiateMaintenanceByName, InitiateMaintenanceInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bf2-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="06bf2-132">-Name</span></span>
<span data-ttu-id="06bf2-133">Yeniden başlatılacak sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06bf2-133">Specifies the name of the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName, InitiateMaintenanceByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bf2-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="06bf2-134">-Profile</span></span>
<span data-ttu-id="06bf2-135">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06bf2-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06bf2-136">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="06bf2-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06bf2-137">-Yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="06bf2-137">-Redeploy</span></span>
<span data-ttu-id="06bf2-138">Cmdlet 'in sanal makineyi yeniden dağıttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06bf2-138">Indicates that the cmdlet redeploys the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06bf2-139">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="06bf2-139">-ServiceName</span></span>
<span data-ttu-id="06bf2-140">Yeniden başlatılacak sanal makineyi içeren Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06bf2-140">Specifies the name of the Azure service that contains the virtual machine to restart.</span></span>

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

### <span data-ttu-id="06bf2-141">-VM</span><span class="sxs-lookup"><span data-stu-id="06bf2-141">-VM</span></span>
<span data-ttu-id="06bf2-142">Sanal makineyi yeniden başlatılacak şekilde tanımlayan sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06bf2-142">Specifies a virtual machine object that identifies the virtual machine to restart.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: RestartInput, RedeployInput, InitiateMaintenanceInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06bf2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06bf2-143">CommonParameters</span></span>
<span data-ttu-id="06bf2-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06bf2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06bf2-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06bf2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06bf2-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06bf2-146">INPUTS</span></span>

## <span data-ttu-id="06bf2-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06bf2-147">OUTPUTS</span></span>

## <span data-ttu-id="06bf2-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06bf2-148">NOTES</span></span>

## <span data-ttu-id="06bf2-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06bf2-149">RELATED LINKS</span></span>

[<span data-ttu-id="06bf2-150">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06bf2-150">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="06bf2-151">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06bf2-151">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="06bf2-152">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06bf2-152">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="06bf2-153">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06bf2-153">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="06bf2-154">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06bf2-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


