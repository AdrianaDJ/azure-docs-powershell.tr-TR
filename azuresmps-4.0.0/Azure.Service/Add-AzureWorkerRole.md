---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105710"
---
# <span data-ttu-id="c2c29-101">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="c2c29-101">Add-AzureWorkerRole</span></span>

## <span data-ttu-id="c2c29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2c29-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c29-103">Özel bir çalışan rolü için gerekli dosyaları ve yapılandırmayı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2c29-103">Creates required files and configuration for a custom worker role.</span></span>

## <span data-ttu-id="c2c29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2c29-104">SYNTAX</span></span>

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c2c29-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2c29-105">DESCRIPTION</span></span>
<span data-ttu-id="c2c29-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c2c29-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c2c29-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c2c29-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c2c29-108">**Add-AzureWorkerRole** cmdlet 'i, özel bir çalışan rolü için bazen scafkatlama olarak da adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="c2c29-108">The **Add-AzureWorkerRole** cmdlet creates required files and configuration, sometimes referred to as scaffolding, for a custom worker role.</span></span>

## <span data-ttu-id="c2c29-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2c29-109">EXAMPLES</span></span>

### <span data-ttu-id="c2c29-110">Örnek 1: tek bir örnek çalışanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c2c29-110">Example 1: Create a single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

<span data-ttu-id="c2c29-111">Bu örnek, geçerli uygulamaya MyWorkerRole adlı tek bir çalışan rolü için scafkatlama ekler.</span><span class="sxs-lookup"><span data-stu-id="c2c29-111">This example adds scaffolding for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="c2c29-112">Örnek 2: birden çok örnek çalışanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c2c29-112">Example 2: Create a multiple instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="c2c29-113">Bu örnek, geçerli uygulamaya MyWorkerRole adlı yeni bir çalışan rolü için, rol örneği sayısı 2 olan bir scafkatlama ekler.</span><span class="sxs-lookup"><span data-stu-id="c2c29-113">This example adds scaffolding for a new worker role named MyWorkerRole to the current application, with a role instance count of 2.</span></span>

### <span data-ttu-id="c2c29-114">Örnek 3: özel dolandırıcılarla çalışan rolü oluşturma</span><span class="sxs-lookup"><span data-stu-id="c2c29-114">Example 3: Create worker role with custom scaffolding</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

<span data-ttu-id="c2c29-115">Bu örnek özel dolandırıcılarla bir çalışan rolü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2c29-115">This example creates a worker role with custom scaffolding.</span></span>

## <span data-ttu-id="c2c29-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2c29-116">PARAMETERS</span></span>

### <span data-ttu-id="c2c29-117">-Örnekler</span><span class="sxs-lookup"><span data-stu-id="c2c29-117">-Instances</span></span>
<span data-ttu-id="c2c29-118">Bu çalışan rolünün rol örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2c29-118">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="c2c29-119">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="c2c29-119">The default is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c29-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2c29-120">-Name</span></span>
<span data-ttu-id="c2c29-121">Çalışan rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2c29-121">Specifies the name of the worker role.</span></span>
<span data-ttu-id="c2c29-122">Bu değer, çalışan rolünde barındırılan özel uygulama için scaflesi içeren klasör adını belirler.</span><span class="sxs-lookup"><span data-stu-id="c2c29-122">This value determines the folder name that contains the scaffolding for the custom application that will be hosted in the worker role.</span></span>
<span data-ttu-id="c2c29-123">Varsayılan, Workerrolen ' dır; burada sayı, hizmette çalışan rollerin sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="c2c29-123">The default is WorkerRolenumber, where number is the number of worker roles in the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c29-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="c2c29-124">-Profile</span></span>
<span data-ttu-id="c2c29-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2c29-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c2c29-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c2c29-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2c29-127">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="c2c29-127">-TemplateFolder</span></span>
<span data-ttu-id="c2c29-128">Çalışan rolünü oluştururken kullanılacak scafkatlama şablonu klasörünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2c29-128">Specifies the scaffolding template folder to be used to create the worker role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c29-129">CommonParameters</span></span>
<span data-ttu-id="c2c29-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2c29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c29-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c29-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c29-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2c29-132">INPUTS</span></span>

## <span data-ttu-id="c2c29-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2c29-133">OUTPUTS</span></span>

## <span data-ttu-id="c2c29-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2c29-134">NOTES</span></span>

## <span data-ttu-id="c2c29-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2c29-135">RELATED LINKS</span></span>

[<span data-ttu-id="c2c29-136">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="c2c29-136">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="c2c29-137">Yeni-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="c2c29-137">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


