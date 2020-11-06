---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 10874ffbb0846765bfbeae06ae4522989280e428
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588267"
---
# <span data-ttu-id="01516-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="01516-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="01516-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01516-102">SYNOPSIS</span></span>
<span data-ttu-id="01516-103">AEM uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="01516-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01516-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01516-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01516-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01516-105">DESCRIPTION</span></span>
<span data-ttu-id="01516-106">**Get-AzureRmVMAEMExtension** cmdlet 'ı, Azure Gelişmiş izleme (AEM) uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="01516-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="01516-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01516-107">EXAMPLES</span></span>

### <span data-ttu-id="01516-108">Örnek 1: AEM uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="01516-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="01516-109">Bu komut contoso-Server adlı sanal makinenin AEM uzantısı için bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="01516-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="01516-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01516-110">PARAMETERS</span></span>

### <span data-ttu-id="01516-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01516-111">-DefaultProfile</span></span>
<span data-ttu-id="01516-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01516-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01516-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="01516-113">-Name</span></span>
<span data-ttu-id="01516-114">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01516-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="01516-115">Bu cmdlet, bu cmdlet 'in belirttiği sanal makinedeki AEM uzantısı için bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="01516-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01516-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="01516-116">-OSType</span></span>
<span data-ttu-id="01516-117">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="01516-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="01516-118">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="01516-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="01516-119">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="01516-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01516-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01516-120">-ResourceGroupName</span></span>
<span data-ttu-id="01516-121">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01516-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="01516-122">Bu cmdlet, bu sanal makinedeki AEM uzantısı için bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="01516-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="01516-123">-Durum</span><span class="sxs-lookup"><span data-stu-id="01516-123">-Status</span></span>
<span data-ttu-id="01516-124">Bu cmdlet 'in yalnızca AEM uzantısının örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01516-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01516-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="01516-125">-VMName</span></span>
<span data-ttu-id="01516-126">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01516-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="01516-127">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="01516-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="01516-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01516-128">CommonParameters</span></span>
<span data-ttu-id="01516-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01516-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01516-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01516-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01516-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01516-131">INPUTS</span></span>

## <span data-ttu-id="01516-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01516-132">OUTPUTS</span></span>

## <span data-ttu-id="01516-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01516-133">NOTES</span></span>

## <span data-ttu-id="01516-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01516-134">RELATED LINKS</span></span>

[<span data-ttu-id="01516-135">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="01516-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="01516-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="01516-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="01516-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="01516-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


