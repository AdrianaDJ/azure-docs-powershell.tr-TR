---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105741"
---
# <span data-ttu-id="0c510-101">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0c510-101">Stop-AzureVM</span></span>

## <span data-ttu-id="0c510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c510-102">SYNOPSIS</span></span>
<span data-ttu-id="0c510-103">Bir Azure sanal makinesini kapatır.</span><span class="sxs-lookup"><span data-stu-id="0c510-103">Shuts down an Azure virtual machine.</span></span>

## <span data-ttu-id="0c510-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c510-104">SYNTAX</span></span>

### <span data-ttu-id="0c510-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c510-105">ByName (Default)</span></span>
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0c510-106">Girdiden</span><span class="sxs-lookup"><span data-stu-id="0c510-106">Input</span></span>
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c510-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c510-107">DESCRIPTION</span></span>
<span data-ttu-id="0c510-108">**Stop-AzureVM** cmdlet 'i bir sanal makineyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="0c510-108">The **Stop-AzureVM** cmdlet shuts down a virtual machine.</span></span>

## <span data-ttu-id="0c510-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c510-109">EXAMPLES</span></span>

### <span data-ttu-id="0c510-110">Örnek 1: sanal makineyi kapatma</span><span class="sxs-lookup"><span data-stu-id="0c510-110">Example 1: Shut down a virtual machine</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

<span data-ttu-id="0c510-111">Bu komut belirtilen hizmetin içerdiği bir sanal makineyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="0c510-111">This command shuts down a virtual machine that the specified service contains.</span></span>

### <span data-ttu-id="0c510-112">Örnek 2: sanal makine nesnesini kullanarak sanal makineyi kapatma</span><span class="sxs-lookup"><span data-stu-id="0c510-112">Example 2: Shut down a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

<span data-ttu-id="0c510-113">Bu komut, **Get-AzureVM** döndüren sanal makine nesnesini kullanarak belirtilen hizmetin içerdiği bir sanal makineyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="0c510-113">This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that **Get-AzureVM** returns.</span></span>

### <span data-ttu-id="0c510-114">Örnek 3: VM 'yi kapatma ve VM 'yi sağlandı</span><span class="sxs-lookup"><span data-stu-id="0c510-114">Example 3: Shut down a VM and keep the VM provisioned</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

<span data-ttu-id="0c510-115">Bu komut belirtilen hizmetin içerdiği bir sanal makineyi kapatır ve bu hizmeti sağladı.</span><span class="sxs-lookup"><span data-stu-id="0c510-115">This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.</span></span>

### <span data-ttu-id="0c510-116">Örnek 4: sanal makineyi kapatma ve dağıtımdaki son VM 'yi ayırmayı verme</span><span class="sxs-lookup"><span data-stu-id="0c510-116">Example 4: Shut down a VM and allow deallocation of the last VM in the deployment</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

<span data-ttu-id="0c510-117">Bu komut, belirtilen hizmetin içerdiği bir sanal makineyi kapatır ve dağıtımdaki son sanal makinenin yeniden oluşturulmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0c510-117">This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.</span></span>

### <span data-ttu-id="0c510-118">Örnek 5: birden çok VM 'yi kapatma</span><span class="sxs-lookup"><span data-stu-id="0c510-118">Example 5: Shut down multiple VMs</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

<span data-ttu-id="0c510-119">Bu komut, belirtilen hizmetin içerdiği birden çok sanal makineyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="0c510-119">This command shuts down multiple virtual machines that the specified service contains.</span></span>

## <span data-ttu-id="0c510-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c510-120">PARAMETERS</span></span>

### <span data-ttu-id="0c510-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0c510-121">-Force</span></span>
<span data-ttu-id="0c510-122">Dağıtımdaki son sanal makinenin ayırmayı kaldırma izni verip vermeyeceğinizi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c510-122">Specifies whether to allow the deallocation of the last virtual machine in a deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c510-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="0c510-123">-InformationAction</span></span>
<span data-ttu-id="0c510-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c510-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0c510-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0c510-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c510-126">'A</span><span class="sxs-lookup"><span data-stu-id="0c510-126">Continue</span></span>
- <span data-ttu-id="0c510-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="0c510-127">Ignore</span></span>
- <span data-ttu-id="0c510-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="0c510-128">Inquire</span></span>
- <span data-ttu-id="0c510-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="0c510-129">SilentlyContinue</span></span>
- <span data-ttu-id="0c510-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="0c510-130">Stop</span></span>
- <span data-ttu-id="0c510-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="0c510-131">Suspend</span></span>

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

### <span data-ttu-id="0c510-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="0c510-132">-InformationVariable</span></span>
<span data-ttu-id="0c510-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c510-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0c510-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c510-134">-Name</span></span>
<span data-ttu-id="0c510-135">Kapatılacak sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c510-135">Specifies the name of the virtual machine to shut down.</span></span>

<span data-ttu-id="0c510-136">Birden çok sanal makineyi zaman uyumsuz olarak durdurmak için joker karakter kullanın.</span><span class="sxs-lookup"><span data-stu-id="0c510-136">Use the wildcard character to stop multiple virtual machines asynchronously.</span></span>
<span data-ttu-id="0c510-137">Joker karakterle, bu cmdlet, kapatma https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) rolü işlemi yerine ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0c510-137">With a wildcard character, this cmdlet calls the Shutdown Roleshttps://msdn.microsoft.com/en-us/library/azure/dn469421.aspx operation (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Rolehttps://msdn.microsoft.com/en-us/library/azure/jj157195.aspx operation (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c510-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="0c510-138">-Profile</span></span>
<span data-ttu-id="0c510-139">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c510-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c510-140">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0c510-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0c510-141">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="0c510-141">-ServiceName</span></span>
<span data-ttu-id="0c510-142">Kapatılacak sanal makineyi içeren Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c510-142">Specifies the name of the Azure service that contains the virtual machine to shut down.</span></span>

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

### <span data-ttu-id="0c510-143">-Staysağlandı</span><span class="sxs-lookup"><span data-stu-id="0c510-143">-StayProvisioned</span></span>
<span data-ttu-id="0c510-144">Bu cmdlet 'in, sanal makinenin sağlandığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c510-144">Specifies that this cmdlet keeps the virtual machine provisioned.</span></span>

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

### <span data-ttu-id="0c510-145">-VM</span><span class="sxs-lookup"><span data-stu-id="0c510-145">-VM</span></span>
<span data-ttu-id="0c510-146">Kapatılacak sanal makineyi tanımlayan sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c510-146">Specifies a virtual machine object that identifies the virtual machine to shut down.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c510-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c510-147">CommonParameters</span></span>
<span data-ttu-id="0c510-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c510-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c510-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c510-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c510-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c510-150">INPUTS</span></span>

## <span data-ttu-id="0c510-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c510-151">OUTPUTS</span></span>

## <span data-ttu-id="0c510-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c510-152">NOTES</span></span>

## <span data-ttu-id="0c510-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c510-153">RELATED LINKS</span></span>

[<span data-ttu-id="0c510-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0c510-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="0c510-155">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0c510-155">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="0c510-156">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0c510-156">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="0c510-157">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0c510-157">Start-AzureVM</span></span>](./Start-AzureVM.md)


