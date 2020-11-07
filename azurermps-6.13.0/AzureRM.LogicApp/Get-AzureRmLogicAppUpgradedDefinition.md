---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
ms.openlocfilehash: b0f4569c123a483db1cceffbcdfd68ef8835a31b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764949"
---
# <span data-ttu-id="d8eaa-101">Get-AzureRmLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="d8eaa-101">Get-AzureRmLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="d8eaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="d8eaa-103">Bir mantık uygulamasının yükseltilmiş tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-103">Gets the upgraded definition for a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8eaa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8eaa-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8eaa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="d8eaa-106">**Get-Azurermlogicappyükseltilmedi Deddefinition** cmdlet 'i, kaynak grubundan şema sürümü ve mantık uygulamasının yükseltilmiş tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-106">The **Get-AzureRmLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="d8eaa-107">Bu cmdlet, yükseltilen mantık uygulamasının tanımını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="d8eaa-108">Kaynak Grup adını, mantık uygulama adını ve hedef şema sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="d8eaa-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d8eaa-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d8eaa-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d8eaa-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d8eaa-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8eaa-113">EXAMPLES</span></span>

### <span data-ttu-id="d8eaa-114">Örnek 1: mantık uygulaması yükseltilmiş tanımını alma</span><span class="sxs-lookup"><span data-stu-id="d8eaa-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
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

<span data-ttu-id="d8eaa-115">İlk komut belirtilen hedef şema sürümüne yükseltilen mantık uygulamasının tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="d8eaa-116">Komut $UpgradedDefinition değişkeninde tanımı depolar.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="d8eaa-117">İkinci komut $UpgradedDefinition içeriğini dize olarak görüntüler.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="d8eaa-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8eaa-118">PARAMETERS</span></span>

### <span data-ttu-id="d8eaa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8eaa-119">-DefaultProfile</span></span>
<span data-ttu-id="d8eaa-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d8eaa-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8eaa-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8eaa-121">-Name</span></span>
<span data-ttu-id="d8eaa-122">Mantık uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="d8eaa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8eaa-123">-ResourceGroupName</span></span>
<span data-ttu-id="d8eaa-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d8eaa-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="d8eaa-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="d8eaa-126">Tanımın hedef şema sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-126">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="d8eaa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8eaa-127">CommonParameters</span></span>
<span data-ttu-id="d8eaa-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8eaa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8eaa-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8eaa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8eaa-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8eaa-130">INPUTS</span></span>

### <span data-ttu-id="d8eaa-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d8eaa-131">System.String</span></span>

## <span data-ttu-id="d8eaa-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8eaa-132">OUTPUTS</span></span>

### <span data-ttu-id="d8eaa-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="d8eaa-133">System.Object</span></span>

## <span data-ttu-id="d8eaa-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8eaa-134">NOTES</span></span>

## <span data-ttu-id="d8eaa-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8eaa-135">RELATED LINKS</span></span>

[<span data-ttu-id="d8eaa-136">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d8eaa-136">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)


