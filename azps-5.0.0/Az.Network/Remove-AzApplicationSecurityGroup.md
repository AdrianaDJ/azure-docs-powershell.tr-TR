---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275961"
---
# <span data-ttu-id="a6cbf-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a6cbf-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="a6cbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="a6cbf-103">Uygulama güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-103">Removes an application security group.</span></span>

## <span data-ttu-id="a6cbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6cbf-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6cbf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6cbf-105">DESCRIPTION</span></span>
<span data-ttu-id="a6cbf-106">**Remove-AzApplicationSecurityGroup** cmdlet 'i uygulama güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="a6cbf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6cbf-107">EXAMPLES</span></span>

### <span data-ttu-id="a6cbf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a6cbf-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a6cbf-109">Bu komut MyResourceGroup adlı kaynak grubunda MyApplicationSecurityGrouo adlı bir uygulama güvenlik grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a6cbf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6cbf-110">PARAMETERS</span></span>

### <span data-ttu-id="a6cbf-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="a6cbf-111">-AsJob</span></span>
<span data-ttu-id="a6cbf-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a6cbf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6cbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6cbf-113">-DefaultProfile</span></span>
<span data-ttu-id="a6cbf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6cbf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a6cbf-115">-Force</span></span>
<span data-ttu-id="a6cbf-116">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="a6cbf-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="a6cbf-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6cbf-117">-Name</span></span>
<span data-ttu-id="a6cbf-118">Uygulama güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="a6cbf-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a6cbf-119">-PassThru</span></span>
<span data-ttu-id="a6cbf-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a6cbf-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a6cbf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6cbf-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6cbf-123">Uygulama güvenlik grubunun kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="a6cbf-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6cbf-124">-Confirm</span></span>
<span data-ttu-id="a6cbf-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6cbf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6cbf-126">-WhatIf</span></span>
<span data-ttu-id="a6cbf-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6cbf-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6cbf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6cbf-129">CommonParameters</span></span>
<span data-ttu-id="a6cbf-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6cbf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6cbf-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6cbf-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6cbf-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6cbf-132">INPUTS</span></span>

### <span data-ttu-id="a6cbf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a6cbf-133">System.String</span></span>

## <span data-ttu-id="a6cbf-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6cbf-134">OUTPUTS</span></span>

### <span data-ttu-id="a6cbf-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6cbf-135">System.Boolean</span></span>

## <span data-ttu-id="a6cbf-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6cbf-136">NOTES</span></span>

## <span data-ttu-id="a6cbf-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6cbf-137">RELATED LINKS</span></span>

[<span data-ttu-id="a6cbf-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a6cbf-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="a6cbf-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a6cbf-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
