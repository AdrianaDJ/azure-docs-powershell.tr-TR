---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267310"
---
# <span data-ttu-id="16d25-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="16d25-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="16d25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16d25-102">SYNOPSIS</span></span>
<span data-ttu-id="16d25-103">Bir mantık uygulaması çalıştırmasında bir eylem alır.</span><span class="sxs-lookup"><span data-stu-id="16d25-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="16d25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16d25-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16d25-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16d25-105">DESCRIPTION</span></span>
<span data-ttu-id="16d25-106">**Get-Azlogicapprunactıon** cmdlet 'i, mantık uygulamasından bir eylem alır.</span><span class="sxs-lookup"><span data-stu-id="16d25-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="16d25-107">Bu cmdlet bir **Workflowrunaction** nesneleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="16d25-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="16d25-108">Mantık uygulaması, kaynak grubu ve Çalıştır seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="16d25-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="16d25-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="16d25-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="16d25-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="16d25-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="16d25-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="16d25-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="16d25-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="16d25-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="16d25-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16d25-113">EXAMPLES</span></span>

### <span data-ttu-id="16d25-114">Örnek 1: bir mantık uygulamasından eylem alma</span><span class="sxs-lookup"><span data-stu-id="16d25-114">Example 1: Get an action from a Logic App run</span></span>
```powershell
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

<span data-ttu-id="16d25-115">Bu komut, LogicAppRun56 adındaki Çalıştır için LogicApp05 adındaki mantık uygulamasından belirli bir mantık uygulaması eylemini alır.</span><span class="sxs-lookup"><span data-stu-id="16d25-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="16d25-116">Örnek 2: bir mantık uygulamasından tüm eylemleri alma</span><span class="sxs-lookup"><span data-stu-id="16d25-116">Example 2: Get all the actions from a Logic App run</span></span>
```powershell
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

<span data-ttu-id="16d25-117">Bu komut, LogicApp05 adındaki bir mantık uygulamasının LogicAppRun56 adındaki Çalıştır adındaki tüm mantık uygulaması eylemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="16d25-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="16d25-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="16d25-118">Example 3</span></span>

<span data-ttu-id="16d25-119">Bu komut, LogicApp05 adındaki bir mantık uygulamasının LogicAppRun56 adındaki Çalıştır adındaki tüm mantık uygulaması eylemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="16d25-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="16d25-120">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="16d25-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="16d25-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16d25-121">PARAMETERS</span></span>

### <span data-ttu-id="16d25-122">-ActionName</span><span class="sxs-lookup"><span data-stu-id="16d25-122">-ActionName</span></span>
<span data-ttu-id="16d25-123">Mantık uygulaması çalıştırmasında bir eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16d25-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="16d25-124">Bu cmdlet, bu parametrenin belirttiği eylemi alır.</span><span class="sxs-lookup"><span data-stu-id="16d25-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="16d25-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d25-125">-DefaultProfile</span></span>
<span data-ttu-id="16d25-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16d25-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16d25-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="16d25-127">-Name</span></span>
<span data-ttu-id="16d25-128">Bu cmdlet 'in eylem aldığı bir mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16d25-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="16d25-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d25-129">-ResourceGroupName</span></span>
<span data-ttu-id="16d25-130">Bu cmdlet 'in eylem aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16d25-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="16d25-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="16d25-131">-RunName</span></span>
<span data-ttu-id="16d25-132">Mantık uygulamasının bir çalıştırmanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16d25-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="16d25-133">Bu cmdlet, bu parametrenin belirttiği bir eylem alır.</span><span class="sxs-lookup"><span data-stu-id="16d25-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="16d25-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d25-134">CommonParameters</span></span>
<span data-ttu-id="16d25-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16d25-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d25-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d25-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d25-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16d25-137">INPUTS</span></span>

### <span data-ttu-id="16d25-138">System. String</span><span class="sxs-lookup"><span data-stu-id="16d25-138">System.String</span></span>

## <span data-ttu-id="16d25-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16d25-139">OUTPUTS</span></span>

### <span data-ttu-id="16d25-140">Microsoft. Azure. Management. Logic. modeller. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="16d25-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="16d25-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16d25-141">NOTES</span></span>

## <span data-ttu-id="16d25-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16d25-142">RELATED LINKS</span></span>

[<span data-ttu-id="16d25-143">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="16d25-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="16d25-144">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="16d25-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


