---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 48121e165eea27b57ec36301a657a6778f4c14b7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939089"
---
# <span data-ttu-id="ae243-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ae243-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="ae243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae243-102">SYNOPSIS</span></span>
<span data-ttu-id="ae243-103">Uygulama güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae243-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae243-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae243-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae243-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae243-105">DESCRIPTION</span></span>
<span data-ttu-id="ae243-106">**Remove-AzureRmApplicationSecurityGroup** cmdlet 'i uygulama güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae243-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="ae243-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae243-107">EXAMPLES</span></span>

### <span data-ttu-id="ae243-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ae243-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ae243-109">Bu komut MyResourceGroup adlı kaynak grubunda MyApplicationSecurityGrouo adlı bir uygulama güvenlik grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="ae243-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ae243-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae243-110">PARAMETERS</span></span>

### <span data-ttu-id="ae243-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae243-111">-DefaultProfile</span></span>
<span data-ttu-id="ae243-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae243-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae243-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ae243-113">-Force</span></span>
<span data-ttu-id="ae243-114">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="ae243-114">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae243-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae243-115">-Name</span></span>
<span data-ttu-id="ae243-116">Uygulama güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ae243-116">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae243-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ae243-117">-PassThru</span></span>
<span data-ttu-id="ae243-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ae243-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ae243-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ae243-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae243-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae243-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae243-121">Uygulama güvenlik grubunun kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ae243-121">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae243-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="ae243-122">-Confirm</span></span>
<span data-ttu-id="ae243-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ae243-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae243-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae243-124">-WhatIf</span></span>
<span data-ttu-id="ae243-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae243-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae243-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ae243-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae243-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae243-127">CommonParameters</span></span>
<span data-ttu-id="ae243-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae243-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae243-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae243-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae243-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae243-130">INPUTS</span></span>

### <span data-ttu-id="ae243-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ae243-131">System.String</span></span>

## <span data-ttu-id="ae243-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae243-132">OUTPUTS</span></span>

### <span data-ttu-id="ae243-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="ae243-133">System.Object</span></span>

## <span data-ttu-id="ae243-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae243-134">NOTES</span></span>

## <span data-ttu-id="ae243-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae243-135">RELATED LINKS</span></span>

[<span data-ttu-id="ae243-136">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ae243-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="ae243-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ae243-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
