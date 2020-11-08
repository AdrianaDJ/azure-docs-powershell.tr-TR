---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106012"
---
# <span data-ttu-id="81825-101">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="81825-101">Stop-AzureStorSimpleJob</span></span>

## <span data-ttu-id="81825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81825-102">SYNOPSIS</span></span>
<span data-ttu-id="81825-103">StorSimple işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="81825-103">Stops a StorSimple job.</span></span>

## <span data-ttu-id="81825-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81825-104">SYNTAX</span></span>

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="81825-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81825-105">DESCRIPTION</span></span>
<span data-ttu-id="81825-106">**Stop-AzureStorSimpleJob** cmdlet 'i bir açık StorSimple işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="81825-106">The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.</span></span>
<span data-ttu-id="81825-107">Bir örnek KIMLIĞI veya bir iş adı sağlayarak bir iş belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81825-107">You can specify a jobs by supplying an instance ID or a job name.</span></span>

## <span data-ttu-id="81825-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81825-108">EXAMPLES</span></span>

### <span data-ttu-id="81825-109">Örnek 1: bir cihazın işlerini durdurma</span><span class="sxs-lookup"><span data-stu-id="81825-109">Example 1: Stop jobs for a device</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

<span data-ttu-id="81825-110">Bu komut, **Get-AzureStorSimpleJob** cmdlet 'Ini kullanarak Device07 adlı aygıtın işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="81825-110">This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.</span></span>
<span data-ttu-id="81825-111">Komut, ardışık düzen işlecini kullanarak işleri geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="81825-111">The command passes the jobs to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="81825-112">Geçerli cmdlet, komutun geçtiği tüm işleri durdurur.</span><span class="sxs-lookup"><span data-stu-id="81825-112">The current cmdlet stops any jobs that the command passes to it.</span></span>
<span data-ttu-id="81825-113">Komut *Force* parametresini belirtir ve bu nedenle işi durdurmadan önce onaylamanız istemez.</span><span class="sxs-lookup"><span data-stu-id="81825-113">The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.</span></span>

### <span data-ttu-id="81825-114">Örnek 2: belirli bir işi durdurma</span><span class="sxs-lookup"><span data-stu-id="81825-114">Example 2: Stop a specific job</span></span>
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

<span data-ttu-id="81825-115">Bu komut, belirtilen örnek KIMLIĞINE sahip olan işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="81825-115">This command stops the job that has the specified instance ID.</span></span>

## <span data-ttu-id="81825-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81825-116">PARAMETERS</span></span>

### <span data-ttu-id="81825-117">-Force</span><span class="sxs-lookup"><span data-stu-id="81825-117">-Force</span></span>
<span data-ttu-id="81825-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="81825-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81825-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="81825-119">-InstanceId</span></span>
<span data-ttu-id="81825-120">Durdurulacak cihaz işinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="81825-120">Specifies the ID of the device job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81825-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="81825-121">-Profile</span></span>
<span data-ttu-id="81825-122">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="81825-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="81825-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81825-123">CommonParameters</span></span>
<span data-ttu-id="81825-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81825-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81825-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81825-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81825-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81825-126">INPUTS</span></span>

### <span data-ttu-id="81825-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="81825-127">None</span></span>

## <span data-ttu-id="81825-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81825-128">OUTPUTS</span></span>

### <span data-ttu-id="81825-129">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="81825-129">DeviceJobDetails</span></span>
<span data-ttu-id="81825-130">Bu cmdlet, bu cmdlet 'in durduğu **devicejob** ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="81825-130">This cmdlet gets details of the **DeviceJob** that this cmdlet stops.</span></span>

## <span data-ttu-id="81825-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81825-131">NOTES</span></span>

## <span data-ttu-id="81825-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81825-132">RELATED LINKS</span></span>

[<span data-ttu-id="81825-133">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="81825-133">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


