---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106453"
---
# <span data-ttu-id="bd18b-101">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="bd18b-101">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="bd18b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd18b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd18b-103">StorSimple aygıtından birim kapsayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bd18b-103">Removes a volume container from a StorSimple device.</span></span>

## <span data-ttu-id="bd18b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd18b-104">SYNTAX</span></span>

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bd18b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd18b-105">DESCRIPTION</span></span>
<span data-ttu-id="bd18b-106">**Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet 'ı StorSimple aygıtından bir birim kapsayıcı nesnesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bd18b-106">The **Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet removes a volume container object from a StorSimple device.</span></span>
<span data-ttu-id="bd18b-107">*Force* parametresini belirtmediğiniz sürece bu cmdlet onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd18b-107">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="bd18b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd18b-108">EXAMPLES</span></span>

### <span data-ttu-id="bd18b-109">Örnek 1: ardışık düzeni kullanarak kapsayıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="bd18b-109">Example 1: Remove a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

<span data-ttu-id="bd18b-110">Bu komut, **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet 'ini kullanarak Contoso63-AppVm adlı cihazda Container08 adındaki birim kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="bd18b-110">This command gets the volume container named Container08 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="bd18b-111">Komut, ardışık düzen işlecini kullanarak birim kapsayıcısını geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bd18b-111">The command passes the volume container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bd18b-112">Bu komut, kapsayıcıyı kaldırmak için görevi başlatır ve ardından bir **Taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="bd18b-112">This command starts the task to remove the container, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="bd18b-113">Görevin durumunu görmek için **Get-AzureStorSimpleTask** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bd18b-113">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="bd18b-114">Bu komut *Force* parametresini belirtir; dolayısıyla sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="bd18b-114">This command specifies the *Force* parameter, so it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bd18b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd18b-115">PARAMETERS</span></span>

### <span data-ttu-id="bd18b-116">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="bd18b-116">-DeviceName</span></span>
<span data-ttu-id="bd18b-117">Birim kapsayıcısının kaldırılacağı StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd18b-117">Specifies the name of the StorSimple device on which to the volume container to remove exists.</span></span>

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

### <span data-ttu-id="bd18b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bd18b-118">-Force</span></span>
<span data-ttu-id="bd18b-119">Bu cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd18b-119">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="bd18b-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="bd18b-120">-Profile</span></span>
<span data-ttu-id="bd18b-121">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd18b-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="bd18b-122">-Birimkapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="bd18b-122">-VolumeContainer</span></span>
<span data-ttu-id="bd18b-123">**Datacontainer** nesnesi olarak kaldırılacak birim kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd18b-123">Specifies the volume container to remove, as a **DataContainer** object.</span></span>
<span data-ttu-id="bd18b-124">**Datacontainer** nesnesi almak için **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bd18b-124">To obtain a **DataContainer** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd18b-125">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="bd18b-125">-WaitForComplete</span></span>
<span data-ttu-id="bd18b-126">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd18b-126">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="bd18b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd18b-127">CommonParameters</span></span>
<span data-ttu-id="bd18b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd18b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd18b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd18b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd18b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd18b-130">INPUTS</span></span>

### <span data-ttu-id="bd18b-131">Veri kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="bd18b-131">DataContainer</span></span>
<span data-ttu-id="bd18b-132">Bu cmdlet kaldırılacak **Datacontainer** nesnesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="bd18b-132">This cmdlet accepts a **DataContainer** object to remove.</span></span>

## <span data-ttu-id="bd18b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd18b-133">OUTPUTS</span></span>

### <span data-ttu-id="bd18b-134">Taskstatusınfo</span><span class="sxs-lookup"><span data-stu-id="bd18b-134">TaskStatusInfo</span></span>
<span data-ttu-id="bd18b-135">Bu cmdlet, *Waitforcomplete* parametresini belirtirseniz bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="bd18b-135">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="bd18b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd18b-136">NOTES</span></span>

## <span data-ttu-id="bd18b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd18b-137">RELATED LINKS</span></span>

[<span data-ttu-id="bd18b-138">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="bd18b-138">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="bd18b-139">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="bd18b-139">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


