---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 2c0eb437aaa8a280b970e9c2a210b37b8fbce2d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274483"
---
# <span data-ttu-id="88cae-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="88cae-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="88cae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88cae-102">SYNOPSIS</span></span>
<span data-ttu-id="88cae-103">Bir mantık uygulamasının yükseltilmiş tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="88cae-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="88cae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88cae-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88cae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88cae-105">DESCRIPTION</span></span>
<span data-ttu-id="88cae-106">**Get-Azlogicappyükseltilmedi Deddefinition** cmdlet 'i, kaynak grubundan şema sürümü ve mantık uygulamasının yükseltilmiş tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="88cae-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="88cae-107">Bu cmdlet, yükseltilen mantık uygulamasının tanımını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="88cae-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="88cae-108">Kaynak Grup adını, mantık uygulama adını ve hedef şema sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="88cae-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="88cae-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="88cae-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="88cae-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="88cae-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="88cae-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="88cae-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="88cae-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="88cae-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="88cae-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88cae-113">EXAMPLES</span></span>

### <span data-ttu-id="88cae-114">Örnek 1: mantık uygulaması yükseltilmiş tanımını alma</span><span class="sxs-lookup"><span data-stu-id="88cae-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
$UpgradedDefinition.ToString()
{

  "$schema": "http://schema.management.azure.com/providers/Microsoft.Logic/schemas/2016-06-01/workflowdefinition.json#",

  "contentVersion": "1.0.0.0",

  "parameters": {},

  "triggers": {

    "httpTrigger": {

      "recurrence": {

        "frequency": "Hour",

        "interval": 1

      },

      "type": "Http",

      "inputs": {

        "method": "GET",

        "uri": "http://www.bing.com"

      },

      "conditions": [

        {

          "expression": "@bool('true')" 

        }

      ] 

    },

    "manualTrigger": {

      "type": "Request",

      "kind": "Http"

    }

  },

  "actions": {

    "httpScope": {

      "actions": {

        "http": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    },

    "http1Scope": {

      "actions": {

        "http1": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    }

  },

  "outputs": {

    "output1": {

      "type": "String",

      "value": "true"

    }

  }

}
```

<span data-ttu-id="88cae-115">İlk komut belirtilen hedef şema sürümüne yükseltilen mantık uygulamasının tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="88cae-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="88cae-116">Komut $UpgradedDefinition değişkeninde tanımı depolar.</span><span class="sxs-lookup"><span data-stu-id="88cae-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="88cae-117">İkinci komut $UpgradedDefinition içeriğini dize olarak görüntüler.</span><span class="sxs-lookup"><span data-stu-id="88cae-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="88cae-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88cae-118">PARAMETERS</span></span>

### <span data-ttu-id="88cae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88cae-119">-DefaultProfile</span></span>
<span data-ttu-id="88cae-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="88cae-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88cae-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="88cae-121">-Name</span></span>
<span data-ttu-id="88cae-122">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88cae-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="88cae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88cae-123">-ResourceGroupName</span></span>
<span data-ttu-id="88cae-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88cae-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="88cae-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="88cae-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="88cae-126">Tanımın hedef şema sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="88cae-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88cae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88cae-127">CommonParameters</span></span>
<span data-ttu-id="88cae-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88cae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88cae-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88cae-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88cae-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88cae-130">INPUTS</span></span>

### <span data-ttu-id="88cae-131">System. String</span><span class="sxs-lookup"><span data-stu-id="88cae-131">System.String</span></span>

## <span data-ttu-id="88cae-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88cae-132">OUTPUTS</span></span>

### <span data-ttu-id="88cae-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="88cae-133">System.Object</span></span>

## <span data-ttu-id="88cae-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88cae-134">NOTES</span></span>

## <span data-ttu-id="88cae-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88cae-135">RELATED LINKS</span></span>

[<span data-ttu-id="88cae-136">Get-Azlogicuyg</span><span class="sxs-lookup"><span data-stu-id="88cae-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


