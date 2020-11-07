---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: 4e937bd3ec1c40aaf4b3c1c188b157792c0030bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760141"
---
# <span data-ttu-id="6cc4c-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6cc4c-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="6cc4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc4c-103">Ağ güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-103">Removes a network security group.</span></span>

## <span data-ttu-id="6cc4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6cc4c-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cc4c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6cc4c-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc4c-106">**Remove-AzNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="6cc4c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6cc4c-107">EXAMPLES</span></span>

### <span data-ttu-id="6cc4c-108">Örnek 1: ağ güvenlik grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="6cc4c-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="6cc4c-109">Bu komut, TestRG adlı kaynak grubundaki NSG-FrontEnd adındaki güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="6cc4c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6cc4c-110">PARAMETERS</span></span>

### <span data-ttu-id="6cc4c-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="6cc4c-111">-AsJob</span></span>
<span data-ttu-id="6cc4c-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6cc4c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cc4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc4c-113">-DefaultProfile</span></span>
<span data-ttu-id="6cc4c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cc4c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6cc4c-115">-Force</span></span>
<span data-ttu-id="6cc4c-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6cc4c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6cc4c-117">-Name</span></span>
<span data-ttu-id="6cc4c-118">Bu cmdlet 'in kaldırdığı ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc4c-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6cc4c-119">-PassThru</span></span>
<span data-ttu-id="6cc4c-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6cc4c-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6cc4c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc4c-122">-ResourceGroupName</span></span>
<span data-ttu-id="6cc4c-123">Bu cmdlet 'in uygulamasından ağ güvenlik grubunu kaldıran bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc4c-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="6cc4c-124">-Confirm</span></span>
<span data-ttu-id="6cc4c-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc4c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc4c-126">-WhatIf</span></span>
<span data-ttu-id="6cc4c-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cc4c-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc4c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc4c-129">CommonParameters</span></span>
<span data-ttu-id="6cc4c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6cc4c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc4c-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc4c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc4c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6cc4c-132">INPUTS</span></span>

### <span data-ttu-id="6cc4c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6cc4c-133">System.String</span></span>

## <span data-ttu-id="6cc4c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6cc4c-134">OUTPUTS</span></span>

### <span data-ttu-id="6cc4c-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6cc4c-135">System.Boolean</span></span>

## <span data-ttu-id="6cc4c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6cc4c-136">NOTES</span></span>

## <span data-ttu-id="6cc4c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6cc4c-137">RELATED LINKS</span></span>

[<span data-ttu-id="6cc4c-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6cc4c-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="6cc4c-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6cc4c-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="6cc4c-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6cc4c-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


