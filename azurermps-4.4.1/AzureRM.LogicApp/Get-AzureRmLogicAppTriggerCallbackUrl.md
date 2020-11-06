---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: f9ac8c7d7131b53b04e7da03eeb17aea33507258
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593102"
---
# <span data-ttu-id="aea95-101">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="aea95-101">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="aea95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea95-102">SYNOPSIS</span></span>
<span data-ttu-id="aea95-103">Bir mantık uygulama tetikleyicisi geri çağırma URL 'SI alır.</span><span class="sxs-lookup"><span data-stu-id="aea95-103">Gets a Logic App trigger callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aea95-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aea95-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aea95-105">DESCRIPTION</span></span>
<span data-ttu-id="aea95-106">**Get-AzureRmLogicAppTriggerCallbackUrl** cmdlet 'i kaynak grubundan bir mantık uygulama tetikleyicisi geri çağırması URL 'si alır.</span><span class="sxs-lookup"><span data-stu-id="aea95-106">The **Get-AzureRmLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="aea95-107">Bu cmdlet geri çağırma URL 'sini temsil eden bir **Workflowtriggercallbackurl** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="aea95-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="aea95-108">Kaynak Grup adını, mantık uygulama adını ve tetik adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="aea95-108">Specify the resource group name, logic app name, and trigger name.</span></span>

<span data-ttu-id="aea95-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="aea95-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="aea95-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="aea95-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="aea95-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="aea95-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="aea95-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="aea95-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="aea95-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aea95-113">EXAMPLES</span></span>

### <span data-ttu-id="aea95-114">Örnek 1: mantık uygulama tetikleyicisi geri çağırma URL 'SI alma</span><span class="sxs-lookup"><span data-stu-id="aea95-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="aea95-115">Bu komut, bir mantık uygulama tetikleyicisi geri çağırma URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="aea95-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="aea95-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aea95-116">PARAMETERS</span></span>

### <span data-ttu-id="aea95-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="aea95-117">-Name</span></span>
<span data-ttu-id="aea95-118">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aea95-118">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="aea95-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea95-119">-ResourceGroupName</span></span>
<span data-ttu-id="aea95-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aea95-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aea95-121">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="aea95-121">-TriggerName</span></span>
<span data-ttu-id="aea95-122">Tetikleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aea95-122">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="aea95-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea95-123">-DefaultProfile</span></span>
<span data-ttu-id="aea95-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aea95-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea95-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea95-125">CommonParameters</span></span>
<span data-ttu-id="aea95-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aea95-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea95-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea95-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea95-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aea95-128">INPUTS</span></span>

## <span data-ttu-id="aea95-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aea95-129">OUTPUTS</span></span>

### <span data-ttu-id="aea95-130">Microsoft. Azure. Management. Logic. modeller. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="aea95-130">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="aea95-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aea95-131">NOTES</span></span>

## <span data-ttu-id="aea95-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aea95-132">RELATED LINKS</span></span>

[<span data-ttu-id="aea95-133">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="aea95-133">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)


