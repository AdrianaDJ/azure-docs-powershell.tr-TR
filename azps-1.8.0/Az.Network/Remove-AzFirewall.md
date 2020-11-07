---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: b46540a614f25a3923301e28cd19d8f1b76af53c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760166"
---
# <span data-ttu-id="dc9f8-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dc9f8-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="dc9f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc9f8-102">SYNOPSIS</span></span>
<span data-ttu-id="dc9f8-103">Güvenlik duvarını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-103">Remove a Firewall.</span></span>

## <span data-ttu-id="dc9f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc9f8-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc9f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc9f8-105">DESCRIPTION</span></span>
<span data-ttu-id="dc9f8-106">**Remove-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="dc9f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc9f8-107">EXAMPLES</span></span>

### <span data-ttu-id="dc9f8-108">1: güvenlik duvarı oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="dc9f8-108">1: Create and delete a Firewall</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="dc9f8-109">Bu örnekte bir güvenlik duvarı oluşturulur ve sonra silinir.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="dc9f8-110">Güvenlik duvarını silerken komut istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="dc9f8-111">2: güvenlik duvarını serbest bırakma ve güvenlik duvarını silme</span><span class="sxs-lookup"><span data-stu-id="dc9f8-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="dc9f8-112">Bu örnekte bir güvenlik duvarı alınır, güvenlik duvarını ayırır ve güvenlik duvarı silinir.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="dc9f8-113">Serbest bırakma komutu, çalışan hizmeti kaldırır ancak güvenlik duvarının yapılandırmasını korur.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="dc9f8-114">Kullanıcı Hizmeti yeniden başlatmak istiyorsa, ayırma yöntemi güvenlik duvarında çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="dc9f8-115">Güvenlik duvarını silerken komut istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="dc9f8-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc9f8-116">PARAMETERS</span></span>

### <span data-ttu-id="dc9f8-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="dc9f8-117">-AsJob</span></span>
<span data-ttu-id="dc9f8-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="dc9f8-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc9f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc9f8-119">-DefaultProfile</span></span>
<span data-ttu-id="dc9f8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc9f8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dc9f8-121">-Force</span></span>
<span data-ttu-id="dc9f8-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc9f8-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc9f8-123">-Name</span></span>
<span data-ttu-id="dc9f8-124">Bu cmdlet 'in kaldırdığı güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dc9f8-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dc9f8-125">-PassThru</span></span>
<span data-ttu-id="dc9f8-126">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dc9f8-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc9f8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc9f8-128">-ResourceGroupName</span></span>
<span data-ttu-id="dc9f8-129">Bu cmdlet 'in kaldırdığı güvenlik duvarını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dc9f8-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc9f8-130">-Confirm</span></span>
<span data-ttu-id="dc9f8-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc9f8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc9f8-132">-WhatIf</span></span>
<span data-ttu-id="dc9f8-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc9f8-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc9f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc9f8-135">CommonParameters</span></span>
<span data-ttu-id="dc9f8-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc9f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc9f8-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc9f8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc9f8-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc9f8-138">INPUTS</span></span>

### <span data-ttu-id="dc9f8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc9f8-139">System.String</span></span>

## <span data-ttu-id="dc9f8-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc9f8-140">OUTPUTS</span></span>

### <span data-ttu-id="dc9f8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc9f8-141">System.Boolean</span></span>

## <span data-ttu-id="dc9f8-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc9f8-142">NOTES</span></span>

## <span data-ttu-id="dc9f8-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc9f8-143">RELATED LINKS</span></span>

[<span data-ttu-id="dc9f8-144">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dc9f8-144">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="dc9f8-145">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dc9f8-145">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="dc9f8-146">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dc9f8-146">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
