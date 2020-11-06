---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/test-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: ab4b746b19f42831b690a61e6300b3205cf7d41b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592032"
---
# <span data-ttu-id="0ff22-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0ff22-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="0ff22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ff22-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff22-103">AEM uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="0ff22-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ff22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ff22-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ff22-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ff22-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff22-106">**Test-AzureRmVMAEMExtension** cmdlet 'ı, Azure Gelişmiş izleme (AEM) uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="0ff22-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="0ff22-107">AEM uzantısı performans verilerini toplar.</span><span class="sxs-lookup"><span data-stu-id="0ff22-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="0ff22-108">Bu cmdlet performans verilerinin kullanılabilir olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="0ff22-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="0ff22-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ff22-109">EXAMPLES</span></span>

### <span data-ttu-id="0ff22-110">Örnek 1: AEM uzantısının yapılandırmasını denetleme</span><span class="sxs-lookup"><span data-stu-id="0ff22-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="0ff22-111">Bu komut, Contoso sunucusu adlı sanal makinenin AEM uzantısının yapılandırmasını denetler.</span><span class="sxs-lookup"><span data-stu-id="0ff22-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="0ff22-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ff22-112">PARAMETERS</span></span>

### <span data-ttu-id="0ff22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff22-113">-DefaultProfile</span></span>
<span data-ttu-id="0ff22-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ff22-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff22-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="0ff22-115">-OSType</span></span>
<span data-ttu-id="0ff22-116">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ff22-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="0ff22-117">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0ff22-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="0ff22-118">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="0ff22-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff22-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff22-119">-ResourceGroupName</span></span>
<span data-ttu-id="0ff22-120">Bu cmdlet 'in denetlediği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ff22-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff22-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="0ff22-121">-SkipStorageCheck</span></span>
<span data-ttu-id="0ff22-122">Bu cmdlet 'in depolama yapılandırmasını gözden aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ff22-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff22-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="0ff22-123">-VMName</span></span>
<span data-ttu-id="0ff22-124">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ff22-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0ff22-125">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısını sınar.</span><span class="sxs-lookup"><span data-stu-id="0ff22-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff22-126">-Waittimeınminutes</span><span class="sxs-lookup"><span data-stu-id="0ff22-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="0ff22-127">Depolama yapılandırması denetimi için zaman aşımı süresini dakika olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ff22-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff22-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff22-128">CommonParameters</span></span>
<span data-ttu-id="0ff22-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ff22-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff22-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff22-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff22-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ff22-131">INPUTS</span></span>

### <span data-ttu-id="0ff22-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0ff22-132">System.String</span></span>

## <span data-ttu-id="0ff22-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ff22-133">OUTPUTS</span></span>

### <span data-ttu-id="0ff22-134">Microsoft. Azure. Commands. COMPUTE. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="0ff22-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="0ff22-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ff22-135">NOTES</span></span>

## <span data-ttu-id="0ff22-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ff22-136">RELATED LINKS</span></span>

[<span data-ttu-id="0ff22-137">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0ff22-137">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="0ff22-138">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0ff22-138">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="0ff22-139">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0ff22-139">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)


