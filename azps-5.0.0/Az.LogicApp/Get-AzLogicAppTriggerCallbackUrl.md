---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280157"
---
# <span data-ttu-id="edbb1-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="edbb1-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="edbb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edbb1-102">SYNOPSIS</span></span>
<span data-ttu-id="edbb1-103">Bir mantık uygulama tetikleyicisi geri çağırma URL 'SI alır.</span><span class="sxs-lookup"><span data-stu-id="edbb1-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="edbb1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edbb1-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edbb1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edbb1-105">DESCRIPTION</span></span>
<span data-ttu-id="edbb1-106">**Get-AzLogicAppTriggerCallbackUrl** cmdlet 'i, kaynak grubundan bir mantık App tetik geri arama URL 'si alır.</span><span class="sxs-lookup"><span data-stu-id="edbb1-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="edbb1-107">Bu cmdlet geri çağırma URL 'sini temsil eden bir **Workflowtriggercallbackurl** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="edbb1-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="edbb1-108">Kaynak Grup adını, mantık uygulama adını ve tetik adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="edbb1-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="edbb1-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="edbb1-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="edbb1-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="edbb1-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="edbb1-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="edbb1-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="edbb1-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="edbb1-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="edbb1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edbb1-113">EXAMPLES</span></span>

### <span data-ttu-id="edbb1-114">Örnek 1: mantık uygulama tetikleyicisi geri çağırma URL 'SI alma</span><span class="sxs-lookup"><span data-stu-id="edbb1-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="edbb1-115">Bu komut, bir mantık uygulama tetikleyicisi geri çağırma URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="edbb1-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="edbb1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edbb1-116">PARAMETERS</span></span>

### <span data-ttu-id="edbb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edbb1-117">-DefaultProfile</span></span>
<span data-ttu-id="edbb1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="edbb1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edbb1-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="edbb1-119">-Name</span></span>
<span data-ttu-id="edbb1-120">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edbb1-120">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="edbb1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edbb1-121">-ResourceGroupName</span></span>
<span data-ttu-id="edbb1-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edbb1-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="edbb1-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="edbb1-123">-TriggerName</span></span>
<span data-ttu-id="edbb1-124">Tetikleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edbb1-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="edbb1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbb1-125">CommonParameters</span></span>
<span data-ttu-id="edbb1-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edbb1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbb1-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edbb1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbb1-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edbb1-128">INPUTS</span></span>

### <span data-ttu-id="edbb1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="edbb1-129">System.String</span></span>

## <span data-ttu-id="edbb1-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edbb1-130">OUTPUTS</span></span>

### <span data-ttu-id="edbb1-131">Microsoft. Azure. Management. Logic. modeller. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="edbb1-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="edbb1-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edbb1-132">NOTES</span></span>

## <span data-ttu-id="edbb1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edbb1-133">RELATED LINKS</span></span>

[<span data-ttu-id="edbb1-134">Get-Azıntegrationaccountcallbackurl</span><span class="sxs-lookup"><span data-stu-id="edbb1-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


