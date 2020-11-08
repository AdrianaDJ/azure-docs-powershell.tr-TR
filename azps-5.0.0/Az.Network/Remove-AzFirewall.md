---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279637"
---
# <span data-ttu-id="648b7-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="648b7-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="648b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="648b7-102">SYNOPSIS</span></span>
<span data-ttu-id="648b7-103">Güvenlik duvarını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="648b7-103">Remove a Firewall.</span></span>

## <span data-ttu-id="648b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="648b7-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="648b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="648b7-105">DESCRIPTION</span></span>
<span data-ttu-id="648b7-106">**Remove-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="648b7-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="648b7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="648b7-107">EXAMPLES</span></span>

### <span data-ttu-id="648b7-108">Örnek 1: güvenlik duvarı oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="648b7-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="648b7-109">Bu örnekte bir güvenlik duvarı oluşturulur ve sonra silinir.</span><span class="sxs-lookup"><span data-stu-id="648b7-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="648b7-110">Güvenlik duvarını silerken komut istemini bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="648b7-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="648b7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="648b7-111">PARAMETERS</span></span>

### <span data-ttu-id="648b7-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="648b7-112">-AsJob</span></span>
<span data-ttu-id="648b7-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="648b7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="648b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="648b7-114">-DefaultProfile</span></span>
<span data-ttu-id="648b7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="648b7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="648b7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="648b7-116">-Force</span></span>
<span data-ttu-id="648b7-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="648b7-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="648b7-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="648b7-118">-Name</span></span>
<span data-ttu-id="648b7-119">Bu cmdlet 'in kaldırdığı güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="648b7-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="648b7-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="648b7-120">-PassThru</span></span>
<span data-ttu-id="648b7-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="648b7-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="648b7-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="648b7-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="648b7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="648b7-123">-ResourceGroupName</span></span>
<span data-ttu-id="648b7-124">Bu cmdlet 'in kaldırdığı güvenlik duvarını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="648b7-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="648b7-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="648b7-125">-Confirm</span></span>
<span data-ttu-id="648b7-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="648b7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="648b7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="648b7-127">-WhatIf</span></span>
<span data-ttu-id="648b7-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="648b7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="648b7-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="648b7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="648b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="648b7-130">CommonParameters</span></span>
<span data-ttu-id="648b7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="648b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="648b7-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="648b7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="648b7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="648b7-133">INPUTS</span></span>

### <span data-ttu-id="648b7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="648b7-134">System.String</span></span>

## <span data-ttu-id="648b7-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="648b7-135">OUTPUTS</span></span>

### <span data-ttu-id="648b7-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="648b7-136">System.Boolean</span></span>

## <span data-ttu-id="648b7-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="648b7-137">NOTES</span></span>

## <span data-ttu-id="648b7-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="648b7-138">RELATED LINKS</span></span>

[<span data-ttu-id="648b7-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="648b7-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="648b7-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="648b7-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="648b7-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="648b7-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
