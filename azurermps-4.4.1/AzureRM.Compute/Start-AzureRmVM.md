---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 3091cb877ff792527cf97e3d44b7c363f9dd94b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587995"
---
# <span data-ttu-id="1da4a-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1da4a-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="1da4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1da4a-102">SYNOPSIS</span></span>
<span data-ttu-id="1da4a-103">Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="1da4a-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1da4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1da4a-104">SYNTAX</span></span>

### <span data-ttu-id="1da4a-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1da4a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1da4a-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="1da4a-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1da4a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1da4a-107">DESCRIPTION</span></span>
<span data-ttu-id="1da4a-108">**Start-AzureRmVM** cmdlet 'ı bir Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="1da4a-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="1da4a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1da4a-109">EXAMPLES</span></span>

### <span data-ttu-id="1da4a-110">Örnek 1: sanal makine başlatma</span><span class="sxs-lookup"><span data-stu-id="1da4a-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="1da4a-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="1da4a-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="1da4a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1da4a-112">PARAMETERS</span></span>

### <span data-ttu-id="1da4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da4a-113">-DefaultProfile</span></span>
<span data-ttu-id="1da4a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1da4a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1da4a-115">-ID</span><span class="sxs-lookup"><span data-stu-id="1da4a-115">-Id</span></span>
<span data-ttu-id="1da4a-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1da4a-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1da4a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1da4a-117">-Name</span></span>
<span data-ttu-id="1da4a-118">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="1da4a-118">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1da4a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1da4a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1da4a-120">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1da4a-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1da4a-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="1da4a-121">-Confirm</span></span>
<span data-ttu-id="1da4a-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1da4a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1da4a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1da4a-123">-WhatIf</span></span>
<span data-ttu-id="1da4a-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1da4a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1da4a-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1da4a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1da4a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da4a-126">CommonParameters</span></span>
<span data-ttu-id="1da4a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1da4a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da4a-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1da4a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da4a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1da4a-129">INPUTS</span></span>

## <span data-ttu-id="1da4a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1da4a-130">OUTPUTS</span></span>

## <span data-ttu-id="1da4a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1da4a-131">NOTES</span></span>

## <span data-ttu-id="1da4a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1da4a-132">RELATED LINKS</span></span>

[<span data-ttu-id="1da4a-133">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1da4a-133">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="1da4a-134">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1da4a-134">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="1da4a-135">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1da4a-135">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="1da4a-136">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1da4a-136">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="1da4a-137">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1da4a-137">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="1da4a-138">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1da4a-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


