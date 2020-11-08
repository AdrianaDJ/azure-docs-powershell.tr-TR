---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095913"
---
# <span data-ttu-id="68e6c-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="68e6c-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="68e6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="68e6c-103">Bir kaynak grubundan mantık uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68e6c-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="68e6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68e6c-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e6c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="68e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="68e6c-106">**Remove-Azlogicuyg** cmdlet 'ı, mantık uygulamaları özelliğini kullanarak kaynak grubundan bir mantık uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68e6c-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="68e6c-107">Mantık uygulamasını ve kaynak grubunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="68e6c-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="68e6c-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="68e6c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="68e6c-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="68e6c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="68e6c-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="68e6c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="68e6c-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="68e6c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="68e6c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68e6c-112">EXAMPLES</span></span>

### <span data-ttu-id="68e6c-113">Örnek 1: mantık uygulamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="68e6c-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="68e6c-114">Bu komut, bir kaynak grubundan mantık uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68e6c-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="68e6c-115">Komut *Force* parametresini içerir ve bu komutun sizden onay istemesini önler.</span><span class="sxs-lookup"><span data-stu-id="68e6c-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="68e6c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68e6c-116">PARAMETERS</span></span>

### <span data-ttu-id="68e6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e6c-117">-DefaultProfile</span></span>
<span data-ttu-id="68e6c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="68e6c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68e6c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="68e6c-119">-Force</span></span>
<span data-ttu-id="68e6c-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="68e6c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="68e6c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="68e6c-121">-Name</span></span>
<span data-ttu-id="68e6c-122">Bu cmdlet 'in kaldırıldığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68e6c-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e6c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68e6c-123">-ResourceGroupName</span></span>
<span data-ttu-id="68e6c-124">Bu cmdlet 'in kaldırıldığı mantık uygulamasını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68e6c-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="68e6c-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="68e6c-125">-Confirm</span></span>
<span data-ttu-id="68e6c-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68e6c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68e6c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e6c-127">-WhatIf</span></span>
<span data-ttu-id="68e6c-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68e6c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68e6c-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68e6c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68e6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e6c-130">CommonParameters</span></span>
<span data-ttu-id="68e6c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68e6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e6c-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e6c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e6c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68e6c-133">INPUTS</span></span>

### <span data-ttu-id="68e6c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="68e6c-134">System.String</span></span>

## <span data-ttu-id="68e6c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68e6c-135">OUTPUTS</span></span>

### <span data-ttu-id="68e6c-136">System. void</span><span class="sxs-lookup"><span data-stu-id="68e6c-136">System.Void</span></span>

## <span data-ttu-id="68e6c-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68e6c-137">NOTES</span></span>

## <span data-ttu-id="68e6c-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68e6c-138">RELATED LINKS</span></span>

[<span data-ttu-id="68e6c-139">Get-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="68e6c-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="68e6c-140">Yeni-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="68e6c-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="68e6c-141">Set-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="68e6c-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="68e6c-142">Start-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="68e6c-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


