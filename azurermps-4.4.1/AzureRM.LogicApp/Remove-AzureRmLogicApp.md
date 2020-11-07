---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 6b76440b2d9e61075ac19e5a6fa0846a95a77669
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763711"
---
# <span data-ttu-id="f27ef-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f27ef-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="f27ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f27ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f27ef-103">Bir kaynak grubundan mantık uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f27ef-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f27ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f27ef-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f27ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f27ef-105">DESCRIPTION</span></span>
<span data-ttu-id="f27ef-106">**Remove-Azurermlogicuyg** cmdlet 'ı, mantık uygulamaları özelliğini kullanarak kaynak grubundan bir mantık uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f27ef-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="f27ef-107">Mantık uygulamasını ve kaynak grubunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="f27ef-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="f27ef-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="f27ef-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f27ef-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="f27ef-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f27ef-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="f27ef-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f27ef-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="f27ef-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f27ef-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f27ef-112">EXAMPLES</span></span>

### <span data-ttu-id="f27ef-113">Örnek 1: mantık uygulamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f27ef-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="f27ef-114">Bu komut, bir kaynak grubundan mantık uygulamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f27ef-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="f27ef-115">Komut *Force* parametresini içerir ve bu komutun sizden onay istemesini önler.</span><span class="sxs-lookup"><span data-stu-id="f27ef-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="f27ef-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f27ef-116">PARAMETERS</span></span>

### <span data-ttu-id="f27ef-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f27ef-117">-Force</span></span>
<span data-ttu-id="f27ef-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f27ef-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f27ef-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f27ef-119">-Name</span></span>
<span data-ttu-id="f27ef-120">Bu cmdlet 'in kaldırıldığı mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f27ef-120">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f27ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f27ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="f27ef-122">Bu cmdlet 'in kaldırıldığı mantık uygulamasını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f27ef-122">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f27ef-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f27ef-123">-Confirm</span></span>
<span data-ttu-id="f27ef-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f27ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f27ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f27ef-125">-WhatIf</span></span>
<span data-ttu-id="f27ef-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f27ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f27ef-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f27ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f27ef-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27ef-128">-DefaultProfile</span></span>
<span data-ttu-id="f27ef-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f27ef-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f27ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27ef-130">CommonParameters</span></span>
<span data-ttu-id="f27ef-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f27ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27ef-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f27ef-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27ef-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f27ef-133">INPUTS</span></span>

## <span data-ttu-id="f27ef-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f27ef-134">OUTPUTS</span></span>

### <span data-ttu-id="f27ef-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="f27ef-135">System.Object</span></span>

## <span data-ttu-id="f27ef-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f27ef-136">NOTES</span></span>

## <span data-ttu-id="f27ef-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f27ef-137">RELATED LINKS</span></span>

[<span data-ttu-id="f27ef-138">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f27ef-138">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="f27ef-139">Yeni-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f27ef-139">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="f27ef-140">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f27ef-140">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="f27ef-141">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f27ef-141">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


