---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 61cae1140ef0c46eee5857c15d0b6032a65caeb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760147"
---
# <span data-ttu-id="8a37e-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8a37e-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="8a37e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a37e-102">SYNOPSIS</span></span>
<span data-ttu-id="8a37e-103">Ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8a37e-103">Removes a network interface.</span></span>

## <span data-ttu-id="8a37e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a37e-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a37e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a37e-105">DESCRIPTION</span></span>
<span data-ttu-id="8a37e-106">**Remove-AzNetworkInterface** cmdlet 'ı bir Azure ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8a37e-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="8a37e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a37e-107">EXAMPLES</span></span>

### <span data-ttu-id="8a37e-108">Örnek 1: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="8a37e-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="8a37e-109">Bu komut, kaynak grubundaki ResourceGroup1 NetworkInterface1 ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8a37e-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="8a37e-110">*Force* parametresi kullanılmadığından, kullanıcıdan bu eylemi onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="8a37e-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="8a37e-111">Örnek 2: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="8a37e-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="8a37e-112">Bu komut, kaynak grubu ResourceGroup1 tüm ağ arabirimlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8a37e-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="8a37e-113">*Force* parametresi kullanıldığından, kullanıcıdan onay istenmez.</span><span class="sxs-lookup"><span data-stu-id="8a37e-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="8a37e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a37e-114">PARAMETERS</span></span>

### <span data-ttu-id="8a37e-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="8a37e-115">-AsJob</span></span>
<span data-ttu-id="8a37e-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8a37e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a37e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a37e-117">-DefaultProfile</span></span>
<span data-ttu-id="8a37e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a37e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a37e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8a37e-119">-Force</span></span>
<span data-ttu-id="8a37e-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8a37e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a37e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a37e-121">-Name</span></span>
<span data-ttu-id="8a37e-122">Bu cmdlet 'in kaldırdığı ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a37e-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a37e-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8a37e-123">-PassThru</span></span>
<span data-ttu-id="8a37e-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8a37e-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8a37e-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8a37e-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8a37e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a37e-126">-ResourceGroupName</span></span>
<span data-ttu-id="8a37e-127">Bu cmdlet 'in kaldırıldığı ağ arabirimini içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a37e-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a37e-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a37e-128">-Confirm</span></span>
<span data-ttu-id="8a37e-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a37e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a37e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a37e-130">-WhatIf</span></span>
<span data-ttu-id="8a37e-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a37e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a37e-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a37e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a37e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a37e-133">CommonParameters</span></span>
<span data-ttu-id="8a37e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a37e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a37e-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a37e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a37e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a37e-136">INPUTS</span></span>

### <span data-ttu-id="8a37e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8a37e-137">System.String</span></span>

## <span data-ttu-id="8a37e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a37e-138">OUTPUTS</span></span>

### <span data-ttu-id="8a37e-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a37e-139">System.Boolean</span></span>

## <span data-ttu-id="8a37e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a37e-140">NOTES</span></span>

## <span data-ttu-id="8a37e-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a37e-141">RELATED LINKS</span></span>

[<span data-ttu-id="8a37e-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8a37e-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="8a37e-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8a37e-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="8a37e-144">Set-Azağinterface</span><span class="sxs-lookup"><span data-stu-id="8a37e-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


