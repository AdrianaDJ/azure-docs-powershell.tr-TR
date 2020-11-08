---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106210"
---
# <span data-ttu-id="76969-101">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="76969-101">New-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="76969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76969-102">SYNOPSIS</span></span>
<span data-ttu-id="76969-103">Bir erişim denetimi kaydı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76969-103">Creates an access control record.</span></span>

## <span data-ttu-id="76969-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76969-104">SYNTAX</span></span>

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="76969-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76969-105">DESCRIPTION</span></span>
<span data-ttu-id="76969-106">**New-AzureStorSimpleAccessControlRecord** cmdlet 'i bir erişim denetimi kaydı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76969-106">The **New-AzureStorSimpleAccessControlRecord** cmdlet creates an access control record.</span></span>
<span data-ttu-id="76969-107">Birimleri yapılandırmak için bir **Accesscontrolrecord** nesnesi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76969-107">You can use an **AccessControlRecord** object to configure volumes.</span></span>

## <span data-ttu-id="76969-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76969-108">EXAMPLES</span></span>

### <span data-ttu-id="76969-109">Örnek 1: bir erişim Controlaccess denetim kaydı oluşturma ve resultaccess denetimini bekleme</span><span class="sxs-lookup"><span data-stu-id="76969-109">Example 1: Create an Access Controlaccess control record and wait for the resultaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

<span data-ttu-id="76969-110">Bu komut, Iqn10 adındaki Iscsı başlatıcısı için Acr10 adında bir erişim denetimi kaydı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76969-110">This command creates an access control record named Acr10 for the iSCSI initiator named Iqn10.</span></span>
<span data-ttu-id="76969-111">Bu komut, *waitforcomplete* parametresini belirtir ve bu nedenle, komut işlem tamamlanana kadar bekler ve ardından **taskstatusınfo** nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="76969-111">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="76969-112">Örnek 2: bir erişim denetimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="76969-112">Example 2: Create an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

<span data-ttu-id="76969-113">Bu komut, Iqn11 adındaki Iscsı başlatıcısı için Acr11 adında bir erişim denetimi kaydı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76969-113">This command creates an access control record named Acr11 for the iSCSI initiator named Iqn11.</span></span>
<span data-ttu-id="76969-114">Bu komut *Waitforcomplete* parametresini belirtmez ve bu nedenle komut görevi başlatır ve ardından bir **taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="76969-114">This command does not specify the *WaitForComplete* parameter, and, therefore, the command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="76969-115">Görevin durumunu görmek için **Get-AzureStorSimpleTask** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="76969-115">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="76969-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76969-116">PARAMETERS</span></span>

### <span data-ttu-id="76969-117">-ACRName</span><span class="sxs-lookup"><span data-stu-id="76969-117">-ACRName</span></span>
<span data-ttu-id="76969-118">Erişim denetimi kaydı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="76969-118">Specifies a name for the access control record.</span></span>

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

### <span data-ttu-id="76969-119">-Iqninitiatorname</span><span class="sxs-lookup"><span data-stu-id="76969-119">-IQNInitiatorName</span></span>
<span data-ttu-id="76969-120">Bu cmdlet 'in birime erişim sağladığı Iscsı başlatıcısının tam adını (ıQN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="76969-120">Specifies the iSCSI qualified name (IQN) of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76969-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="76969-121">-Profile</span></span>
<span data-ttu-id="76969-122">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="76969-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="76969-123">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="76969-123">-WaitForComplete</span></span>
<span data-ttu-id="76969-124">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="76969-124">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="76969-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76969-125">CommonParameters</span></span>
<span data-ttu-id="76969-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76969-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76969-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76969-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76969-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76969-128">INPUTS</span></span>

### <span data-ttu-id="76969-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="76969-129">None</span></span>

## <span data-ttu-id="76969-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76969-130">OUTPUTS</span></span>

### <span data-ttu-id="76969-131">Taskstatusınfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="76969-131">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="76969-132">*Waitforcomplete* parametresini belirtirseniz, bu cmdlet bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="76969-132">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="76969-133">Bu parametreyi belirtmezseniz, bir **Taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="76969-133">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="76969-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76969-134">NOTES</span></span>

## <span data-ttu-id="76969-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76969-135">RELATED LINKS</span></span>

[<span data-ttu-id="76969-136">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="76969-136">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="76969-137">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="76969-137">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="76969-138">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="76969-138">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="76969-139">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="76969-139">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


