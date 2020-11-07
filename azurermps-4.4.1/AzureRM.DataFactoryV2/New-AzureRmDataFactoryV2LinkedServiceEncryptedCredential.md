---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 9960a34d19c4016461ddfc53a37f83d3e73e7526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764072"
---
# <span data-ttu-id="01c3d-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="01c3d-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="01c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="01c3d-103">Bağlı hizmette kimlik bilgilerini belirtilen tümleştirme çalışma zamanına göre şifrele.</span><span class="sxs-lookup"><span data-stu-id="01c3d-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01c3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01c3d-104">SYNTAX</span></span>

### <span data-ttu-id="01c3d-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="01c3d-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="01c3d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="01c3d-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="01c3d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="01c3d-107">DESCRIPTION</span></span>
<span data-ttu-id="01c3d-108">New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet 'i, bağlantılı hizmette belirtilen tümleştirme çalışma zamanına sahip kimlik bilgilerini şifreler.</span><span class="sxs-lookup"><span data-stu-id="01c3d-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="01c3d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01c3d-109">EXAMPLES</span></span>

### <span data-ttu-id="01c3d-110">Örnek 1: bağlantılı hizmette creadentials 'i şifrele</span><span class="sxs-lookup"><span data-stu-id="01c3d-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="01c3d-111">Bu komut, D:\sql.jsdosyadaki kimlik bilgilerini Mycır adlı tümleştirme çalışma zamanıyla şifreler.</span><span class="sxs-lookup"><span data-stu-id="01c3d-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="01c3d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01c3d-112">PARAMETERS</span></span>

### <span data-ttu-id="01c3d-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="01c3d-113">-DataFactory</span></span>
<span data-ttu-id="01c3d-114">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="01c3d-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01c3d-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="01c3d-115">-DataFactoryName</span></span>
<span data-ttu-id="01c3d-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="01c3d-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c3d-117">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="01c3d-117">-DefinitionFile</span></span>
<span data-ttu-id="01c3d-118">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="01c3d-118">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c3d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="01c3d-119">-Force</span></span>
<span data-ttu-id="01c3d-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="01c3d-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c3d-121">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="01c3d-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="01c3d-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="01c3d-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c3d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c3d-123">-ResourceGroupName</span></span>
<span data-ttu-id="01c3d-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="01c3d-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c3d-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="01c3d-125">-Confirm</span></span>
<span data-ttu-id="01c3d-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01c3d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c3d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c3d-127">-WhatIf</span></span>
<span data-ttu-id="01c3d-128">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="01c3d-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="01c3d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01c3d-129">INPUTS</span></span>

### <span data-ttu-id="01c3d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="01c3d-130">System.String</span></span>
<span data-ttu-id="01c3d-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="01c3d-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="01c3d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01c3d-132">OUTPUTS</span></span>

### <span data-ttu-id="01c3d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="01c3d-133">System.String</span></span>


## <span data-ttu-id="01c3d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01c3d-134">NOTES</span></span>

## <span data-ttu-id="01c3d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01c3d-135">RELATED LINKS</span></span>

