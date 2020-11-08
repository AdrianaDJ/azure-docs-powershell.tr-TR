---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106389"
---
# <span data-ttu-id="1ca07-101">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="1ca07-101">Add-AzureNodeWorkerRole</span></span>

## <span data-ttu-id="1ca07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ca07-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca07-103">node.exe üzerinden bulutta barındırılmak için Node.js uygulamasının gerekli dosyalarını ve klasörlerini oluşturur</span><span class="sxs-lookup"><span data-stu-id="1ca07-103">Creates the required files and folders for a Node.js application to be hosted in the cloud via node.exe</span></span>

## <span data-ttu-id="1ca07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ca07-104">SYNTAX</span></span>

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ca07-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ca07-105">DESCRIPTION</span></span>
<span data-ttu-id="1ca07-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1ca07-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1ca07-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1ca07-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1ca07-108">**Add-AzureNodeWorkerRole** cmdlet 'i, bir Node.js uygulamasının node.exe ile bulutta barındırılması için, bazen scafkatlama olarak da adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="1ca07-108">The **Add-AzureNodeWorkerRole** cmdlet creates the required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via node.exe.</span></span>

## <span data-ttu-id="1ca07-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ca07-109">EXAMPLES</span></span>

### <span data-ttu-id="1ca07-110">Örnek 1: tek örnekli işçi rolü</span><span class="sxs-lookup"><span data-stu-id="1ca07-110">Example 1: Single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

<span data-ttu-id="1ca07-111">Bu örnek, geçerli uygulamaya **Myworkerrole** adlı tek bir çalışan rolü için scafkatlama ekler.</span><span class="sxs-lookup"><span data-stu-id="1ca07-111">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application.</span></span>

### <span data-ttu-id="1ca07-112">Örnek 2: birden çok örnek çalışanı rolü</span><span class="sxs-lookup"><span data-stu-id="1ca07-112">Example 2: Multiple instance worker role</span></span>
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="1ca07-113">Bu örnek, geçerli uygulamaya **Myworkerrole** adlı tek bir çalışan rolü için, rol örneği sayısı 2 olan bir scafkatlama ekler.</span><span class="sxs-lookup"><span data-stu-id="1ca07-113">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="1ca07-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ca07-114">PARAMETERS</span></span>

### <span data-ttu-id="1ca07-115">-Örnekler</span><span class="sxs-lookup"><span data-stu-id="1ca07-115">-Instances</span></span>
<span data-ttu-id="1ca07-116">Bu çalışan rolünün rol örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ca07-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="1ca07-117">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="1ca07-117">Default is 1.</span></span>

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

### <span data-ttu-id="1ca07-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ca07-118">-Name</span></span>
<span data-ttu-id="1ca07-119">Çalışan rolünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ca07-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="1ca07-120">Değer, çalışan rolünde barındırılan node.js hizmetinin scaflesi içeren klasör adını belirler.</span><span class="sxs-lookup"><span data-stu-id="1ca07-120">The value determines the folder name that contains the scaffolding for the node.js service hosted in the worker role.</span></span>
<span data-ttu-id="1ca07-121">Varsayılan WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="1ca07-121">Default is WorkerRole1.</span></span>

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

### <span data-ttu-id="1ca07-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="1ca07-122">-Profile</span></span>
<span data-ttu-id="1ca07-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ca07-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ca07-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1ca07-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ca07-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca07-125">CommonParameters</span></span>
<span data-ttu-id="1ca07-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ca07-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca07-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ca07-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca07-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ca07-128">INPUTS</span></span>

## <span data-ttu-id="1ca07-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ca07-129">OUTPUTS</span></span>

## <span data-ttu-id="1ca07-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ca07-130">NOTES</span></span>

## <span data-ttu-id="1ca07-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ca07-131">RELATED LINKS</span></span>

[<span data-ttu-id="1ca07-132">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="1ca07-132">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="1ca07-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="1ca07-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


