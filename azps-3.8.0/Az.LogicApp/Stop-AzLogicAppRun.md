---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 9a437d3b8e1803865aedf7e46d0bf879cfcdeab8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095891"
---
# <span data-ttu-id="4189c-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="4189c-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="4189c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4189c-102">SYNOPSIS</span></span>
<span data-ttu-id="4189c-103">Mantık uygulamasının çalıştırılmasını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="4189c-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="4189c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4189c-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4189c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4189c-105">DESCRIPTION</span></span>
<span data-ttu-id="4189c-106">**Stop-AzLogicAppRun** cmdlet 'i, mantık uygulamasının çalıştırılmasını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="4189c-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="4189c-107">Mantık uygulaması, kaynak grubu ve Çalıştır seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="4189c-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="4189c-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="4189c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4189c-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="4189c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4189c-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="4189c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4189c-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="4189c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4189c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4189c-112">EXAMPLES</span></span>

### <span data-ttu-id="4189c-113">Örnek 1: mantık uygulamasının çalıştırılmasını Iptal etme</span><span class="sxs-lookup"><span data-stu-id="4189c-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="4189c-114">Bu komut, LogicApp03 adındaki mantık uygulamasının çalıştırılmasını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="4189c-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="4189c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4189c-115">PARAMETERS</span></span>

### <span data-ttu-id="4189c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4189c-116">-DefaultProfile</span></span>
<span data-ttu-id="4189c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4189c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4189c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4189c-118">-Force</span></span>
<span data-ttu-id="4189c-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4189c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4189c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4189c-120">-Name</span></span>
<span data-ttu-id="4189c-121">Bu cmdlet 'in bir çalıştırmayı iptal ettiğinde bir mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189c-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="4189c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4189c-122">-ResourceGroupName</span></span>
<span data-ttu-id="4189c-123">Bu cmdlet 'in bir çalıştırmayı iptal ettiğinde kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189c-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="4189c-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="4189c-124">-RunName</span></span>
<span data-ttu-id="4189c-125">Bu cmdlet 'in iptal olduğu bir mantık uygulamasının çalışmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4189c-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="4189c-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="4189c-126">-Confirm</span></span>
<span data-ttu-id="4189c-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4189c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4189c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4189c-128">-WhatIf</span></span>
<span data-ttu-id="4189c-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4189c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4189c-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4189c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4189c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4189c-131">CommonParameters</span></span>
<span data-ttu-id="4189c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4189c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4189c-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4189c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4189c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4189c-134">INPUTS</span></span>

### <span data-ttu-id="4189c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4189c-135">System.String</span></span>

## <span data-ttu-id="4189c-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4189c-136">OUTPUTS</span></span>

### <span data-ttu-id="4189c-137">System. void</span><span class="sxs-lookup"><span data-stu-id="4189c-137">System.Void</span></span>

## <span data-ttu-id="4189c-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4189c-138">NOTES</span></span>

## <span data-ttu-id="4189c-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4189c-139">RELATED LINKS</span></span>

[<span data-ttu-id="4189c-140">Start-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="4189c-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


