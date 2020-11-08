---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 1BD296FB-8BFC-473F-951D-D2BF265E50AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 048be9276957ee865aa3204392b1dd847b0d6acf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106449"
---
# <span data-ttu-id="753b3-101">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="753b3-101">Remove-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="753b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="753b3-102">SYNOPSIS</span></span>
<span data-ttu-id="753b3-103">Var olan bir depolama hesabı kimlik bilgisini siler.</span><span class="sxs-lookup"><span data-stu-id="753b3-103">Deletes an existing storage account credential.</span></span>

## <span data-ttu-id="753b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="753b3-104">SYNTAX</span></span>

### <span data-ttu-id="753b3-105">Identifybyname</span><span class="sxs-lookup"><span data-stu-id="753b3-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="753b3-106">Identifybyobject</span><span class="sxs-lookup"><span data-stu-id="753b3-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleStorageAccountCredential -SAC <StorageAccountCredentialResponse> [-WaitForComplete]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="753b3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="753b3-107">DESCRIPTION</span></span>
<span data-ttu-id="753b3-108">**Remove-AzureStorSimpleStorageAccountCredential** cmdlet 'i var olan bir depolama hesabı kimlik bilgisini siler.</span><span class="sxs-lookup"><span data-stu-id="753b3-108">The **Remove-AzureStorSimpleStorageAccountCredential** cmdlet deletes an existing storage account credential.</span></span>
<span data-ttu-id="753b3-109">Bir hesap belirtin veya silinecek **Storageaccountcredential** nesnesini almak için **Get-AzureStorSimpleStorageAccountCredential** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="753b3-109">Specify an account by name or use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet to obtain a **StorageAccountCredential** object to delete.</span></span>

## <span data-ttu-id="753b3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="753b3-110">EXAMPLES</span></span>

### <span data-ttu-id="753b3-111">Örnek 1: depolama hesabı kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="753b3-111">Example 1: Remove a storage account credential</span></span>
```
PS C:\>Remove-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" -Force
VERBOSE: ClientRequestId: 8e10d56b-ddb1-459b-b26e-a185f5a303de_PS
VERBOSE: About to create a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: 55cb6296-0156-4266-8591-d9e9bf8cc584_PS
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
982f4b19-ccb0-4ad3-9b02-f8ad25bf2e72 for tracking the task's status
```

<span data-ttu-id="753b3-112">Bu komut, ContosoStorage07 adlı depolama hesabının hesap kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="753b3-112">This command removes the account credential for the storage account named ContosoStorage07.</span></span>
<span data-ttu-id="753b3-113">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="753b3-113">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="753b3-114">Cmdlet, onayınızı istemeden kimlik bilgisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="753b3-114">The cmdlet removes the credential without prompting your for confirmation.</span></span>

### <span data-ttu-id="753b3-115">Örnek 2: ardışık düzen işlecini kullanarak depolama hesabı kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="753b3-115">Example 2: Remove a storage account credential by using the pipeline operator</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage07" | Remove-AzureStorSimpleStorageAccountCredential -Force -WaitForComplete
VERBOSE: ClientRequestId: f1b46216-bf4c-4c19-8e92-1dfe3894e258_PS
VERBOSE: ClientRequestId: 0d946f8f-c771-4ade-8a83-7c08dad86c52_PS
VERBOSE: ClientRequestId: 2000bab6-8311-4192-ad12-c67e35fc2697_PS
VERBOSE: Storage Access Credential with name ContosoStorage07 found! 
VERBOSE: About to run a job to remove your Storage Access Credential! 
VERBOSE: ClientRequestId: b803b165-bef8-4a8f-9509-4b515ea8bdec_PS
VERBOSE: Your delete operation completed successfully!
```

<span data-ttu-id="753b3-116">Bu komut **Get-AzureStorSimpleStorageAccountCredential** cmdlet 'Ini kullanarak ContosoStorage07 adındaki depolama hesabını alır ve bu nesneyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="753b3-116">This command gets the storage account named ContosoStorage07 by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet, and then passes that object to the current cmdlet.</span></span>
<span data-ttu-id="753b3-117">Geçerli cmdlet söz konusu depolama hesabının kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="753b3-117">The current cmdlet removes the credential for that storage account.</span></span>
<span data-ttu-id="753b3-118">Bu komut, *Waitforcomplete* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="753b3-118">This command specifies the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="753b3-119">Remove işlemini tamamlayana kadar cmdlet denetimi konsola geri döndürmez.</span><span class="sxs-lookup"><span data-stu-id="753b3-119">The cmdlet does not return control to the console until it completes the remove operation.</span></span>

## <span data-ttu-id="753b3-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="753b3-120">PARAMETERS</span></span>

### <span data-ttu-id="753b3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="753b3-121">-Force</span></span>
<span data-ttu-id="753b3-122">Bu cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="753b3-122">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="753b3-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="753b3-123">-Profile</span></span>
<span data-ttu-id="753b3-124">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="753b3-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="753b3-125">-SAC</span><span class="sxs-lookup"><span data-stu-id="753b3-125">-SAC</span></span>
<span data-ttu-id="753b3-126">Kaldırılacak kimlik bilgilerini **Storageaccountcredential** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="753b3-126">Specifies credential, as a **StorageAccountCredential** object, to remove.</span></span>
<span data-ttu-id="753b3-127">**Storageaccountcredential** nesnesi almak Için, **Get-AzureStorSimpleStorageAccountCredential** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="753b3-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="753b3-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="753b3-128">-StorageAccountName</span></span>
<span data-ttu-id="753b3-129">Silinecek depolama hesabı kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="753b3-129">Specifies the name of the storage account credential to delete.</span></span>

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

### <span data-ttu-id="753b3-130">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="753b3-130">-WaitForComplete</span></span>
<span data-ttu-id="753b3-131">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="753b3-131">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="753b3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753b3-132">CommonParameters</span></span>
<span data-ttu-id="753b3-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="753b3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753b3-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="753b3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753b3-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="753b3-135">INPUTS</span></span>

### <span data-ttu-id="753b3-136">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="753b3-136">StorageAccountCredential</span></span>
<span data-ttu-id="753b3-137">Bu cmdlet, ardışık düzeni kullanarak **Storageaccountcredential** nesnesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="753b3-137">This cmdlet accepts a **StorageAccountCredential** object by using the pipeline.</span></span>

## <span data-ttu-id="753b3-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="753b3-138">OUTPUTS</span></span>

### <span data-ttu-id="753b3-139">Taskstatusınfo</span><span class="sxs-lookup"><span data-stu-id="753b3-139">TaskStatusInfo</span></span>
<span data-ttu-id="753b3-140">Bu cmdlet, *Waitforcomplete* parametresini belirtirseniz bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="753b3-140">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="753b3-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="753b3-141">NOTES</span></span>

## <span data-ttu-id="753b3-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="753b3-142">RELATED LINKS</span></span>

[<span data-ttu-id="753b3-143">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="753b3-143">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="753b3-144">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="753b3-144">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="753b3-145">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="753b3-145">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="753b3-146">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="753b3-146">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


