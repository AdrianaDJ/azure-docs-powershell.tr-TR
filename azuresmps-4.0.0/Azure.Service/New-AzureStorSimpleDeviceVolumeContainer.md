---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105520"
---
# <span data-ttu-id="17ec8-101">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="17ec8-101">New-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="17ec8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="17ec8-103">Birim kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17ec8-103">Creates a volume container.</span></span>

## <span data-ttu-id="17ec8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17ec8-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="17ec8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="17ec8-105">DESCRIPTION</span></span>
<span data-ttu-id="17ec8-106">**New-AzureStorSimpleDeviceVolumeContainer** cmdlet 'i bir birim kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17ec8-106">The **New-AzureStorSimpleDeviceVolumeContainer** cmdlet creates a volume container.</span></span>
<span data-ttu-id="17ec8-107">Bir depolama hesabı kimlik bilgisini yeni birim kapsayıcısıyla ilişkilendirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="17ec8-107">You must associate a storage account credential with the new volume container.</span></span>
<span data-ttu-id="17ec8-108">Depolama hesabı kimlik bilgilerini almak için **Get-AzureStorSimpleStorageAccountCredential** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="17ec8-108">To obtain a storage account credential, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

## <span data-ttu-id="17ec8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17ec8-109">EXAMPLES</span></span>

### <span data-ttu-id="17ec8-110">Örnek 1: kapsayıcı oluşturma</span><span class="sxs-lookup"><span data-stu-id="17ec8-110">Example 1: Create a container</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

<span data-ttu-id="17ec8-111">Bu komut, **Get-AzureStorSimpleStorageAccountCredential** cmdlet 'Ini kullanarak contosoaccount adlı hesabın depolama hesabı kimlik bilgisini alır.</span><span class="sxs-lookup"><span data-stu-id="17ec8-111">This command gets the storage account credential for the account named ContosoAccount by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>
<span data-ttu-id="17ec8-112">Komut, ardışık düzen işlecini kullanarak kimlik bilgisini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="17ec8-112">The command passes the credential to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="17ec8-113">Bu cmdlet, Contoso63-AppVm adındaki cihazda Container08 adlı kapsayıcıyı oluşturmak için bu cmdlet 'teki kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="17ec8-113">This cmdlet uses the credential from that cmdlet to create the container named Container08 on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="17ec8-114">Bu komut işi başlatır ve ardından bir **Taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="17ec8-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="17ec8-115">İşin durumunu görmek için **Get-AzureStorSimpleTask** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="17ec8-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="17ec8-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17ec8-116">PARAMETERS</span></span>

### <span data-ttu-id="17ec8-117">-BandWidthRateInMbps</span><span class="sxs-lookup"><span data-stu-id="17ec8-117">-BandWidthRateInMbps</span></span>
<span data-ttu-id="17ec8-118">Saniyede megabit (Mbps) cinsinden bant genişliği hızını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ec8-118">Specifies the bandwidth rate in megabits per second (Mbps).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ec8-119">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="17ec8-119">-DeviceName</span></span>
<span data-ttu-id="17ec8-120">Birim kapsayıcısının oluşturulacağı StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ec8-120">Specifies the name of the StorSimple device on which to create the volume container.</span></span>

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

### <span data-ttu-id="17ec8-121">-EncryptionEnabled</span><span class="sxs-lookup"><span data-stu-id="17ec8-121">-EncryptionEnabled</span></span>
<span data-ttu-id="17ec8-122">Şifrelemenin etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="17ec8-122">Indicates whether to enable encryption.</span></span>

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

### <span data-ttu-id="17ec8-123">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="17ec8-123">-EncryptionKey</span></span>
<span data-ttu-id="17ec8-124">Şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ec8-124">Specifies the encryption key.</span></span>

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

### <span data-ttu-id="17ec8-125">-PrimaryStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="17ec8-125">-PrimaryStorageAccountCredential</span></span>
<span data-ttu-id="17ec8-126">Yeni birim kapsayıcısıyla ilişkilendirilecek bir **Storageaccountcredential** nesnesi olarak kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ec8-126">Specifies the credential, as a **StorageAccountCredential** object, to associate with the new volume container.</span></span>
<span data-ttu-id="17ec8-127">**Storageaccountcredential** nesnesi almak Için, **Get-AzureStorSimpleStorageAccountCredential** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="17ec8-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17ec8-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="17ec8-128">-Profile</span></span>
<span data-ttu-id="17ec8-129">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ec8-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="17ec8-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="17ec8-130">-VolumeContainerName</span></span>
<span data-ttu-id="17ec8-131">Oluşturulacak birim kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ec8-131">Specifies the name of the volume container to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ec8-132">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="17ec8-132">-WaitForComplete</span></span>
<span data-ttu-id="17ec8-133">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="17ec8-133">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="17ec8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ec8-134">CommonParameters</span></span>
<span data-ttu-id="17ec8-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17ec8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ec8-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17ec8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ec8-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17ec8-137">INPUTS</span></span>

### <span data-ttu-id="17ec8-138">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="17ec8-138">StorageAccountCredential</span></span>
<span data-ttu-id="17ec8-139">Bu cmdlet, birim kapsayıcısıyla ilişkilendirilecek bir **Primarystorageaccountcredential** nesnesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="17ec8-139">This cmdlet accepts a **PrimaryStorageAccountCredential** object to associate with the volume container.</span></span>

## <span data-ttu-id="17ec8-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17ec8-140">OUTPUTS</span></span>

### <span data-ttu-id="17ec8-141">Taskstatusınfo</span><span class="sxs-lookup"><span data-stu-id="17ec8-141">TaskStatusInfo</span></span>
<span data-ttu-id="17ec8-142">Bu cmdlet, *Waitforcomplete* parametresini belirtirseniz bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="17ec8-142">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="17ec8-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17ec8-143">NOTES</span></span>

## <span data-ttu-id="17ec8-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17ec8-144">RELATED LINKS</span></span>

[<span data-ttu-id="17ec8-145">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="17ec8-145">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="17ec8-146">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="17ec8-146">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="17ec8-147">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="17ec8-147">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="17ec8-148">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="17ec8-148">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


