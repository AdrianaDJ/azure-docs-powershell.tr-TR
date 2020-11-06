---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: e75c34d76c304af272655c3e4e81fcfd547d11b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592637"
---
# <span data-ttu-id="af6b3-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="af6b3-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="af6b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="af6b3-103">Sanal makineden AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af6b3-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af6b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af6b3-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af6b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="af6b3-106">**Remove-AzureRmVMAEMExtension** cmdlet 'i bir sanal makineden Azure Gelişmiş izleme (AEM) uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af6b3-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="af6b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af6b3-107">EXAMPLES</span></span>

### <span data-ttu-id="af6b3-108">Örnek 1: AEM uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="af6b3-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="af6b3-109">Bu komut contoso-Server adlı sanal makinenin AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af6b3-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="af6b3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af6b3-110">PARAMETERS</span></span>

### <span data-ttu-id="af6b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af6b3-111">-DefaultProfile</span></span>
<span data-ttu-id="af6b3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af6b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af6b3-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="af6b3-113">-Name</span></span>
<span data-ttu-id="af6b3-114">Bu cmdlet 'in AEM uzantısını kaldıran sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af6b3-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="af6b3-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="af6b3-115">-OSType</span></span>
<span data-ttu-id="af6b3-116">İşletim sistemi diskinin işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="af6b3-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="af6b3-117">İşletim sistemi diskinin türü yoksa, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="af6b3-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="af6b3-118">Bu parametre için kabul edilebilir değerler: Windows ve Linux.</span><span class="sxs-lookup"><span data-stu-id="af6b3-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="af6b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af6b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="af6b3-120">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af6b3-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="af6b3-121">Bu cmdlet, bu sanal makineden AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af6b3-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="af6b3-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="af6b3-122">-VMName</span></span>
<span data-ttu-id="af6b3-123">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af6b3-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="af6b3-124">Bu cmdlet, bu parametrenin belirttiği sanal makinenin AEM uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af6b3-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="af6b3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af6b3-125">CommonParameters</span></span>
<span data-ttu-id="af6b3-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af6b3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af6b3-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af6b3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af6b3-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af6b3-128">INPUTS</span></span>

## <span data-ttu-id="af6b3-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af6b3-129">OUTPUTS</span></span>

## <span data-ttu-id="af6b3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af6b3-130">NOTES</span></span>

## <span data-ttu-id="af6b3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af6b3-131">RELATED LINKS</span></span>

[<span data-ttu-id="af6b3-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="af6b3-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="af6b3-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="af6b3-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="af6b3-134">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="af6b3-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


