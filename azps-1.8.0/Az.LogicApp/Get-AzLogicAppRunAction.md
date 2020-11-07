---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 46f0afa20fbc8e7d8ac659f4fcb13a10591aa79f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916083"
---
# <span data-ttu-id="e2818-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="e2818-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="e2818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2818-102">SYNOPSIS</span></span>
<span data-ttu-id="e2818-103">Bir mantık uygulaması çalıştırmasında bir eylem alır.</span><span class="sxs-lookup"><span data-stu-id="e2818-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="e2818-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2818-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2818-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2818-105">DESCRIPTION</span></span>
<span data-ttu-id="e2818-106">**Get-Azlogicapprunactıon** cmdlet 'i, mantık uygulamasından bir eylem alır.</span><span class="sxs-lookup"><span data-stu-id="e2818-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="e2818-107">Bu cmdlet bir **Workflowrunaction** nesneleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e2818-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="e2818-108">Mantık uygulaması, kaynak grubu ve Çalıştır seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e2818-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="e2818-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="e2818-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e2818-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="e2818-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e2818-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="e2818-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e2818-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="e2818-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e2818-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2818-113">EXAMPLES</span></span>

### <span data-ttu-id="e2818-114">Örnek 1: bir mantık uygulamasından eylem alma</span><span class="sxs-lookup"><span data-stu-id="e2818-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="e2818-115">Bu komut, LogicAppRun56 adındaki Çalıştır için LogicApp05 adındaki mantık uygulamasından belirli bir mantık uygulaması eylemini alır.</span><span class="sxs-lookup"><span data-stu-id="e2818-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="e2818-116">Örnek 2: bir mantık uygulamasından tüm eylemleri alma</span><span class="sxs-lookup"><span data-stu-id="e2818-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="e2818-117">Bu komut, LogicApp05 adındaki bir mantık uygulamasının LogicAppRun56 adındaki Çalıştır adındaki tüm mantık uygulaması eylemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e2818-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="e2818-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2818-118">PARAMETERS</span></span>

### <span data-ttu-id="e2818-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="e2818-119">-ActionName</span></span>
<span data-ttu-id="e2818-120">Mantık uygulaması çalıştırmasında bir eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2818-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="e2818-121">Bu cmdlet, bu parametrenin belirttiği eylemi alır.</span><span class="sxs-lookup"><span data-stu-id="e2818-121">This cmdlet gets the action that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2818-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2818-122">-DefaultProfile</span></span>
<span data-ttu-id="e2818-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e2818-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2818-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2818-124">-Name</span></span>
<span data-ttu-id="e2818-125">Bu cmdlet 'in eylem aldığı bir mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2818-125">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="e2818-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2818-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2818-127">Bu cmdlet 'in eylem aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2818-127">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="e2818-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="e2818-128">-RunName</span></span>
<span data-ttu-id="e2818-129">Mantık uygulamasının bir çalıştırmanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2818-129">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="e2818-130">Bu cmdlet, bu parametrenin belirttiği bir eylem alır.</span><span class="sxs-lookup"><span data-stu-id="e2818-130">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="e2818-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2818-131">CommonParameters</span></span>
<span data-ttu-id="e2818-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2818-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2818-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2818-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2818-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2818-134">INPUTS</span></span>

### <span data-ttu-id="e2818-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e2818-135">System.String</span></span>

## <span data-ttu-id="e2818-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2818-136">OUTPUTS</span></span>

### <span data-ttu-id="e2818-137">Microsoft. Azure. Management. Logic. modeller. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="e2818-137">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="e2818-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2818-138">NOTES</span></span>

## <span data-ttu-id="e2818-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2818-139">RELATED LINKS</span></span>

[<span data-ttu-id="e2818-140">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="e2818-140">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="e2818-141">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="e2818-141">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


