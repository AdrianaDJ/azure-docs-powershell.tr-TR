---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: c6c2c356557d2d9d40a4012a7deee5aec0e73aa4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595153"
---
# <span data-ttu-id="d1c3a-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="d1c3a-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="d1c3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c3a-103">Mantık uygulamasının çalıştırılmasını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1c3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1c3a-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1c3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1c3a-105">DESCRIPTION</span></span>
<span data-ttu-id="d1c3a-106">**Stop-AzureRmLogicAppRun** cmdlet 'i, mantık uygulamasının çalıştırılmasını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="d1c3a-107">Mantık uygulaması, kaynak grubu ve Çalıştır seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-107">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="d1c3a-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d1c3a-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d1c3a-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d1c3a-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d1c3a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1c3a-112">EXAMPLES</span></span>

### <span data-ttu-id="d1c3a-113">Örnek 1: mantık uygulamasının çalıştırılmasını Iptal etme</span><span class="sxs-lookup"><span data-stu-id="d1c3a-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076"
```

<span data-ttu-id="d1c3a-114">Bu komut, LogicApp03 adındaki mantık uygulamasının çalıştırılmasını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="d1c3a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1c3a-115">PARAMETERS</span></span>

### <span data-ttu-id="d1c3a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d1c3a-116">-Force</span></span>
<span data-ttu-id="d1c3a-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d1c3a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d1c3a-118">-Name</span></span>
<span data-ttu-id="d1c3a-119">Bu cmdlet 'in bir çalıştırmayı iptal ettiğinde bir mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-119">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="d1c3a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c3a-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1c3a-121">Bu cmdlet 'in bir çalıştırmayı iptal ettiğinde kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-121">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="d1c3a-122">-RunName</span><span class="sxs-lookup"><span data-stu-id="d1c3a-122">-RunName</span></span>
<span data-ttu-id="d1c3a-123">Bu cmdlet 'in iptal olduğu bir mantık uygulamasının çalışmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-123">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="d1c3a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1c3a-124">-Confirm</span></span>
<span data-ttu-id="d1c3a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1c3a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1c3a-126">-WhatIf</span></span>
<span data-ttu-id="d1c3a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1c3a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1c3a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c3a-129">-DefaultProfile</span></span>
<span data-ttu-id="d1c3a-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1c3a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c3a-131">CommonParameters</span></span>
<span data-ttu-id="d1c3a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1c3a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c3a-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1c3a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c3a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1c3a-134">INPUTS</span></span>

## <span data-ttu-id="d1c3a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1c3a-135">OUTPUTS</span></span>

### <span data-ttu-id="d1c3a-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="d1c3a-136">System.Object</span></span>

## <span data-ttu-id="d1c3a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1c3a-137">NOTES</span></span>

## <span data-ttu-id="d1c3a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1c3a-138">RELATED LINKS</span></span>

[<span data-ttu-id="d1c3a-139">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d1c3a-139">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


