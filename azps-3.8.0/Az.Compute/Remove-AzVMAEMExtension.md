---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097594"
---
# <span data-ttu-id="689e2-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="689e2-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="689e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="689e2-102">SYNOPSIS</span></span>
<span data-ttu-id="689e2-103">Sanal makineden AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="689e2-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="689e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="689e2-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="689e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="689e2-105">DESCRIPTION</span></span>
<span data-ttu-id="689e2-106">**Remove-AzVMAEMExtension** cmdlet 'i bir sanal makineden Azure Gelişmiş izleme (AEM) uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="689e2-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="689e2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="689e2-107">EXAMPLES</span></span>

### <span data-ttu-id="689e2-108">Örnek 1: AEM uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="689e2-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="689e2-109">Bu komut contoso-Server adlı sanal makinenin AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="689e2-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="689e2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="689e2-110">PARAMETERS</span></span>

### <span data-ttu-id="689e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689e2-111">-DefaultProfile</span></span>
<span data-ttu-id="689e2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="689e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689e2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="689e2-113">-Name</span></span>
<span data-ttu-id="689e2-114">Bu cmdlet 'in AEM uzantısını kaldıran sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="689e2-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="689e2-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="689e2-115">-NoWait</span></span>
<span data-ttu-id="689e2-116">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="689e2-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="689e2-117">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="689e2-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689e2-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="689e2-118">-OSType</span></span>
<span data-ttu-id="689e2-119">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="689e2-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="689e2-120">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="689e2-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="689e2-121">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="689e2-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="689e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="689e2-123">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="689e2-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="689e2-124">Bu cmdlet, bu sanal makineden AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="689e2-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="689e2-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="689e2-125">-VMName</span></span>
<span data-ttu-id="689e2-126">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="689e2-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="689e2-127">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="689e2-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="689e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689e2-128">CommonParameters</span></span>
<span data-ttu-id="689e2-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="689e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689e2-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="689e2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689e2-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="689e2-131">INPUTS</span></span>

### <span data-ttu-id="689e2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="689e2-132">System.String</span></span>

## <span data-ttu-id="689e2-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="689e2-133">OUTPUTS</span></span>

### <span data-ttu-id="689e2-134">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="689e2-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="689e2-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="689e2-135">NOTES</span></span>

## <span data-ttu-id="689e2-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="689e2-136">RELATED LINKS</span></span>

[<span data-ttu-id="689e2-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="689e2-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="689e2-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="689e2-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="689e2-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="689e2-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


