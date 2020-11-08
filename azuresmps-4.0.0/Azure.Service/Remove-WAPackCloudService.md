---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1ECF6BB5-3751-4DA0-AC6C-A64F15F46D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552c2511a806abb4329860e7c15d8a68b5e03f79
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107413"
---
# <span data-ttu-id="e0477-101">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e0477-101">Remove-WAPackCloudService</span></span>

## <span data-ttu-id="e0477-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0477-102">SYNOPSIS</span></span>
<span data-ttu-id="e0477-103">Bulut hizmeti nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0477-103">Removes cloud service objects.</span></span>

## <span data-ttu-id="e0477-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0477-104">SYNTAX</span></span>

```
Remove-WAPackCloudService -CloudService <CloudService> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0477-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0477-105">DESCRIPTION</span></span>
<span data-ttu-id="e0477-106">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e0477-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e0477-107">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e0477-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e0477-108">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e0477-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e0477-109">**Remove-WAPackCloudService** cmdlet 'i bulut hizmeti nesnelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0477-109">The **Remove-WAPackCloudService** cmdlet removes cloud service objects.</span></span>

## <span data-ttu-id="e0477-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0477-110">EXAMPLES</span></span>

### <span data-ttu-id="e0477-111">Örnek 1: bulut hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="e0477-111">Example 1: Remove a cloud service</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService01"
PS C:\> Remove-WAPackVM -VM $CloudService
```

<span data-ttu-id="e0477-112">İlk komut ContosoCloudService01 adındaki bulut hizmetini **Get-WAPackCloudService** cmdlet 'ini kullanarak alır ve bu nesneyi $CloudService değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e0477-112">The first command gets the cloud service named ContosoCloudService01 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="e0477-113">İkinci komut $CloudService depolanan CloudService öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0477-113">The second command removes the cloudservice stored in $CloudService.</span></span>
<span data-ttu-id="e0477-114">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0477-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="e0477-115">Örnek 2: onaysız bir bulut hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="e0477-115">Example 2: Remove a cloud service without confirmation</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService02"
PS C:\> Remove-WAPackCloudService -VM $CloudService -Force
```

<span data-ttu-id="e0477-116">İlk komut ContosoCloudService02 adındaki bulut hizmetini **Get-WAPackCloudService** cmdlet 'ini kullanarak alır ve bu nesneyi $CloudService değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e0477-116">The first command gets the cloud service named ContosoCloudService02 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="e0477-117">İkinci komut, $CloudService depolanan bulut hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0477-117">The second command removes the cloud service stored in $CloudService.</span></span>
<span data-ttu-id="e0477-118">Bu komut *Force* parametresini içerir.</span><span class="sxs-lookup"><span data-stu-id="e0477-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="e0477-119">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="e0477-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e0477-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0477-120">PARAMETERS</span></span>

### <span data-ttu-id="e0477-121">-CloudService</span><span class="sxs-lookup"><span data-stu-id="e0477-121">-CloudService</span></span>
<span data-ttu-id="e0477-122">Bulut hizmeti nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0477-122">Specifies a cloud service object.</span></span>
<span data-ttu-id="e0477-123">Bulut hizmeti edinmek için **Get-WAPackCloudService** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e0477-123">To obtain a cloud service, use the **Get-WAPackCloudService** cmdlet.</span></span>

```yaml
Type: CloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0477-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e0477-124">-Force</span></span>
<span data-ttu-id="e0477-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e0477-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0477-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e0477-126">-PassThru</span></span>
<span data-ttu-id="e0477-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e0477-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e0477-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e0477-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e0477-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="e0477-129">-Profile</span></span>
<span data-ttu-id="e0477-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0477-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0477-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e0477-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0477-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0477-132">-Confirm</span></span>
<span data-ttu-id="e0477-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0477-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0477-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0477-134">-WhatIf</span></span>
<span data-ttu-id="e0477-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0477-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0477-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0477-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0477-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0477-137">CommonParameters</span></span>
<span data-ttu-id="e0477-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0477-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0477-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0477-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0477-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0477-140">INPUTS</span></span>

## <span data-ttu-id="e0477-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0477-141">OUTPUTS</span></span>

## <span data-ttu-id="e0477-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0477-142">NOTES</span></span>

## <span data-ttu-id="e0477-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0477-143">RELATED LINKS</span></span>

[<span data-ttu-id="e0477-144">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e0477-144">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="e0477-145">Yeni-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e0477-145">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)


