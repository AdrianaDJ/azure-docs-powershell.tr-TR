---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/test-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: ae4a6d72fcb44406773234b6de55cec7ccef8eb9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940166"
---
# <span data-ttu-id="a3a4b-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a3a4b-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="a3a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a4b-103">AEM uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3a4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3a4b-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3a4b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3a4b-105">DESCRIPTION</span></span>
<span data-ttu-id="a3a4b-106">**Test-AzureRmVMAEMExtension** cmdlet 'ı, Azure Gelişmiş izleme (AEM) uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="a3a4b-107">AEM uzantısı performans verilerini toplar.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="a3a4b-108">Bu cmdlet performans verilerinin kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="a3a4b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3a4b-109">EXAMPLES</span></span>

### <span data-ttu-id="a3a4b-110">Örnek 1: AEM uzantısının yapılandırmasını denetleme</span><span class="sxs-lookup"><span data-stu-id="a3a4b-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="a3a4b-111">Bu komut, Contoso sunucusu adlı sanal makinenin AEM uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="a3a4b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3a4b-112">PARAMETERS</span></span>

### <span data-ttu-id="a3a4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a4b-113">-DefaultProfile</span></span>
<span data-ttu-id="a3a4b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a4b-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="a3a4b-115">-OSType</span></span>
<span data-ttu-id="a3a4b-116">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="a3a4b-117">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="a3a4b-118">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a4b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a4b-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3a4b-120">Bu cmdlet 'in denetlediği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="a3a4b-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="a3a4b-121">-SkipStorageCheck</span></span>
<span data-ttu-id="a3a4b-122">Bu cmdlet 'in depolama yapılandırmasını gözden aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a4b-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="a3a4b-123">-VMName</span></span>
<span data-ttu-id="a3a4b-124">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a3a4b-125">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısını sınar.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a4b-126">-Waittimeınminutes</span><span class="sxs-lookup"><span data-stu-id="a3a4b-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="a3a4b-127">Depolama yapılandırması denetimi için zaman aşımı süresini dakika olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a4b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a4b-128">CommonParameters</span></span>
<span data-ttu-id="a3a4b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a4b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3a4b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a4b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3a4b-131">INPUTS</span></span>

### <span data-ttu-id="a3a4b-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a3a4b-132">None</span></span>
<span data-ttu-id="a3a4b-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a3a4b-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3a4b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3a4b-134">OUTPUTS</span></span>

### <span data-ttu-id="a3a4b-135">Microsoft. Azure. Commands. COMPUTE. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="a3a4b-135">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="a3a4b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3a4b-136">NOTES</span></span>

## <span data-ttu-id="a3a4b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3a4b-137">RELATED LINKS</span></span>

[<span data-ttu-id="a3a4b-138">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a3a4b-138">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="a3a4b-139">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a3a4b-139">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="a3a4b-140">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a3a4b-140">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


