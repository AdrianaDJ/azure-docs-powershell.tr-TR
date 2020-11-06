---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 47121a8a06e2b4aa4e48218d1be4694743c00de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586734"
---
# <span data-ttu-id="be621-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="be621-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="be621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be621-102">SYNOPSIS</span></span>
<span data-ttu-id="be621-103">Bağlı hizmette kimlik bilgilerini belirtilen tümleştirme çalışma zamanına göre şifrele.</span><span class="sxs-lookup"><span data-stu-id="be621-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be621-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be621-104">SYNTAX</span></span>

### <span data-ttu-id="be621-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be621-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be621-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="be621-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be621-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="be621-107">DESCRIPTION</span></span>
<span data-ttu-id="be621-108">New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet 'i, bağlantılı hizmette belirtilen tümleştirme çalışma zamanına sahip kimlik bilgilerini şifreler.</span><span class="sxs-lookup"><span data-stu-id="be621-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="be621-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be621-109">EXAMPLES</span></span>

### <span data-ttu-id="be621-110">Örnek 1: bağlantılı hizmette creadentials 'i şifrele</span><span class="sxs-lookup"><span data-stu-id="be621-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="be621-111">Bu komut, D:\sql.jsdosyadaki kimlik bilgilerini Mycır adlı tümleştirme çalışma zamanıyla şifreler.</span><span class="sxs-lookup"><span data-stu-id="be621-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="be621-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be621-112">PARAMETERS</span></span>

### <span data-ttu-id="be621-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="be621-113">-DataFactory</span></span>
<span data-ttu-id="be621-114">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="be621-114">The data factory object.</span></span>

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

### <span data-ttu-id="be621-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="be621-115">-DataFactoryName</span></span>
<span data-ttu-id="be621-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="be621-116">The data factory name.</span></span>

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

### <span data-ttu-id="be621-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be621-117">-DefaultProfile</span></span>
<span data-ttu-id="be621-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be621-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be621-119">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="be621-119">-DefinitionFile</span></span>
<span data-ttu-id="be621-120">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="be621-120">The JSON file path.</span></span>

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

### <span data-ttu-id="be621-121">-Force</span><span class="sxs-lookup"><span data-stu-id="be621-121">-Force</span></span>
<span data-ttu-id="be621-122">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="be621-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="be621-123">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="be621-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="be621-124">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="be621-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="be621-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be621-125">-ResourceGroupName</span></span>
<span data-ttu-id="be621-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="be621-126">The resource group name.</span></span>

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

### <span data-ttu-id="be621-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="be621-127">-Confirm</span></span>
<span data-ttu-id="be621-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be621-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be621-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be621-129">-WhatIf</span></span>
<span data-ttu-id="be621-130">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="be621-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="be621-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be621-131">CommonParameters</span></span>
<span data-ttu-id="be621-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be621-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be621-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be621-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be621-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be621-134">INPUTS</span></span>

### <span data-ttu-id="be621-135">System. String</span><span class="sxs-lookup"><span data-stu-id="be621-135">System.String</span></span>
<span data-ttu-id="be621-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="be621-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="be621-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be621-137">OUTPUTS</span></span>

### <span data-ttu-id="be621-138">System. String</span><span class="sxs-lookup"><span data-stu-id="be621-138">System.String</span></span>

## <span data-ttu-id="be621-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be621-139">NOTES</span></span>

## <span data-ttu-id="be621-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be621-140">RELATED LINKS</span></span>

