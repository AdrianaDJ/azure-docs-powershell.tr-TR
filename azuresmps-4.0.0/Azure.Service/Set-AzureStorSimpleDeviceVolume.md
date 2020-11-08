---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 39E9BB88-6AD8-4B05-9498-35393E22BA30
online version: ''
schema: 2.0.0
ms.openlocfilehash: 234b1f7fa2719cc1b34e6bcd0b8e8fd340acc4af
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106418"
---
# <span data-ttu-id="91590-101">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="91590-101">Set-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="91590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91590-102">SYNOPSIS</span></span>
<span data-ttu-id="91590-103">Var olan bir birimin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="91590-103">Updates the properties of an existing volume.</span></span>

## <span data-ttu-id="91590-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91590-104">SYNTAX</span></span>

### <span data-ttu-id="91590-105">Identifybyname</span><span class="sxs-lookup"><span data-stu-id="91590-105">IdentifyByName</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="91590-106">Identifybyobject</span><span class="sxs-lookup"><span data-stu-id="91590-106">IdentifyByObject</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="91590-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="91590-107">DESCRIPTION</span></span>
<span data-ttu-id="91590-108">**Set-AzureStorSimpleDeviceVolume** cmdlet 'i mevcut bir birimin özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="91590-108">The **Set-AzureStorSimpleDeviceVolume** cmdlet updates the properties of an existing volume.</span></span>
<span data-ttu-id="91590-109">Bu cmdlet, bir birimi bir veya daha fazla erişim denetimi kaydı ile ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="91590-109">This cmdlet associates a volume with one or more access control records.</span></span>
<span data-ttu-id="91590-110">**Accesscontrolrecord** nesnelerini almak için **Get-AzureStorSimpleAccessControlRecord** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="91590-110">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="91590-111">Birimin boyutunu veya türünü güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="91590-111">Update the size or type for the volume.</span></span>
<span data-ttu-id="91590-112">Ayrıca, birimi çevrimiçi oluşturmayı de güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="91590-112">Also, update whether to create the volume online.</span></span>

## <span data-ttu-id="91590-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91590-113">EXAMPLES</span></span>

### <span data-ttu-id="91590-114">Örnek 1: bir birimin çevrimiçi değerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="91590-114">Example 1: Update online value for a volume</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $False
VERBOSE: ClientRequestId: f2869570-ea47-4be7-801e-9c0f22f2600d_PS
VERBOSE: ClientRequestId: c70bb86a-51d3-4390-be17-4d0847641dc3_PS
VERBOSE: ClientRequestId: d20cb5b2-6b3c-4e06-af99-cada28c5e50a_PS
VERBOSE: ClientRequestId: ab6d533e-b55b-4cfb-9c58-9153295e0547_PS
de7000f1-29c7-4102-a375-b52432f9e67e
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
de7000f1-29c7-4102-a375-b52432f9e67e for tracking the task's status
```

<span data-ttu-id="91590-115">Bu komut, Volume18 adlı birimi $False çevrimiçi değeri olacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="91590-115">This command updates the volume named Volume18 to have an online value of $False.</span></span>
<span data-ttu-id="91590-116">Bu komut görevi başlatır ve bir **Taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="91590-116">This command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="91590-117">Görevin durumunu görmek için **Get-AzureStorSimpleTask** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="91590-117">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="91590-118">Örnek 2: çevrimiçi değeri değiştirme ve türü</span><span class="sxs-lookup"><span data-stu-id="91590-118">Example 2: Modify online value and type</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $True -VolumeAppType ArchiveVolume 
VERBOSE: ClientRequestId: af42b02a-645e-4801-a2d7-4197511c68cf_PS
VERBOSE: ClientRequestId: 7cb4f3b4-548e-42dc-a38c-0df0911c5206_PS
VERBOSE: ClientRequestId: 7cc706ad-a58f-4939-8e78-cabae8379a51_PS
VERBOSE: ClientRequestId: 6bed21d5-12fc-4a12-a89c-120bdb5636b1_PS
aa977225-af78-4c93-b754-72704afc928f
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
aa977225-af78-4c93-b754-72704afc928f for tracking the task's status
```

<span data-ttu-id="91590-119">Bu komut, Volume18 adlı birimi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="91590-119">This command updates the volume named Volume18.</span></span>
<span data-ttu-id="91590-120">Türü değiştirir ve *çevrimiçi* parametrenin değerini $true olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="91590-120">It modifies the type and changes the value of the *Online* parameter to $True.</span></span>

## <span data-ttu-id="91590-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91590-121">PARAMETERS</span></span>

### <span data-ttu-id="91590-122">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="91590-122">-AccessControlRecords</span></span>
<span data-ttu-id="91590-123">Birimle ilişkilendirilecek erişim denetimi kayıtlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-123">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91590-124">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="91590-124">-DeviceName</span></span>
<span data-ttu-id="91590-125">Birimin güncelleştirilmesi gereken StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-125">Specifies the name of the StorSimple device on which to update the volume exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91590-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="91590-126">-InformationAction</span></span>
<span data-ttu-id="91590-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="91590-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="91590-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91590-129">'A</span><span class="sxs-lookup"><span data-stu-id="91590-129">Continue</span></span>
- <span data-ttu-id="91590-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="91590-130">Ignore</span></span>
- <span data-ttu-id="91590-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="91590-131">Inquire</span></span>
- <span data-ttu-id="91590-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="91590-132">SilentlyContinue</span></span>
- <span data-ttu-id="91590-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="91590-133">Stop</span></span>
- <span data-ttu-id="91590-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="91590-134">Suspend</span></span>

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

### <span data-ttu-id="91590-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="91590-135">-InformationVariable</span></span>
<span data-ttu-id="91590-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="91590-137">-NewName</span><span class="sxs-lookup"><span data-stu-id="91590-137">-NewName</span></span>
<span data-ttu-id="91590-138">StorSimple cihazı için yeni bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-138">Specifies a new name for the StorSimple device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91590-139">-Çevrimiçi</span><span class="sxs-lookup"><span data-stu-id="91590-139">-Online</span></span>
<span data-ttu-id="91590-140">Birimin çevrimiçi olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-140">Specifies whether the volume is online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91590-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="91590-141">-Profile</span></span>
<span data-ttu-id="91590-142">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-142">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="91590-143">-Hacim</span><span class="sxs-lookup"><span data-stu-id="91590-143">-Volume</span></span>
<span data-ttu-id="91590-144">Güncelleştirilecek birimin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-144">Specifies the name of the volume to update.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91590-145">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="91590-145">-VolumeAppType</span></span>
<span data-ttu-id="91590-146">Birimi birincil veya arşiv birimi olacak şekilde güncelleştirip güncelleştirmeyeceğinizi belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-146">Specifies whether to update the volume to be a primary or archive volume.</span></span>
<span data-ttu-id="91590-147">Geçerli değerler: PrimaryVolume ve ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="91590-147">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91590-148">-BirimAdı</span><span class="sxs-lookup"><span data-stu-id="91590-148">-VolumeName</span></span>
<span data-ttu-id="91590-149">Güncelleştirilecek birimin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-149">Specifies the name of the volume to update.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91590-150">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="91590-150">-VolumeSizeInBytes</span></span>
<span data-ttu-id="91590-151">Birimin güncelleştirilmiş boyutunu bayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="91590-151">Specifies the updated size, in bytes, for the volume.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91590-152">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="91590-152">-WaitForComplete</span></span>
<span data-ttu-id="91590-153">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="91590-153">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91590-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91590-154">CommonParameters</span></span>
<span data-ttu-id="91590-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91590-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91590-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91590-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91590-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91590-157">INPUTS</span></span>

### <span data-ttu-id="91590-158">Listeniz\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="91590-158">List\<AccessControlRecord\></span></span>
<span data-ttu-id="91590-159">Bu cmdlet, birimle ilişkilendirilecek **Accesscontrolrecord** nesnelerinin listesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="91590-159">This cmdlet accepts a list of **AccessControlRecord** objects to associate to a volume.</span></span>

## <span data-ttu-id="91590-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91590-160">OUTPUTS</span></span>

### <span data-ttu-id="91590-161">Taskstatusınfo</span><span class="sxs-lookup"><span data-stu-id="91590-161">TaskStatusInfo</span></span>
<span data-ttu-id="91590-162">Bu cmdlet, *Waitforcomplete* parametresini belirtirseniz bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="91590-162">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="91590-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91590-163">NOTES</span></span>

## <span data-ttu-id="91590-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91590-164">RELATED LINKS</span></span>

[<span data-ttu-id="91590-165">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="91590-165">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="91590-166">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="91590-166">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="91590-167">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="91590-167">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="91590-168">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="91590-168">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="91590-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="91590-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


