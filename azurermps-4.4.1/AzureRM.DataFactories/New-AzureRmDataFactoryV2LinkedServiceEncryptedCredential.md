---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 3face29daf5c6da80e5d6b277850c6639efe96dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762703"
---
# <span data-ttu-id="19735-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="19735-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="19735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19735-102">SYNOPSIS</span></span>
<span data-ttu-id="19735-103">Bağlı hizmette kimlik bilgilerini belirtilen tümleştirme çalışma zamanına göre şifrele.</span><span class="sxs-lookup"><span data-stu-id="19735-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19735-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19735-104">SYNTAX</span></span>

### <span data-ttu-id="19735-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19735-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19735-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="19735-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19735-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="19735-107">DESCRIPTION</span></span>
<span data-ttu-id="19735-108">New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet 'i, bağlantılı hizmette belirtilen tümleştirme çalışma zamanına sahip kimlik bilgilerini şifreler.</span><span class="sxs-lookup"><span data-stu-id="19735-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="19735-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19735-109">EXAMPLES</span></span>

### <span data-ttu-id="19735-110">Örnek 1: bağlantılı hizmette creadentials 'i şifrele</span><span class="sxs-lookup"><span data-stu-id="19735-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="19735-111">Bu komut, D:\sql.jsdosyadaki kimlik bilgilerini Mycır adlı tümleştirme çalışma zamanıyla şifreler.</span><span class="sxs-lookup"><span data-stu-id="19735-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="19735-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19735-112">PARAMETERS</span></span>

### <span data-ttu-id="19735-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="19735-113">-DataFactory</span></span>
<span data-ttu-id="19735-114">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="19735-114">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19735-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="19735-115">-DataFactoryName</span></span>
<span data-ttu-id="19735-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="19735-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19735-117">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="19735-117">-DefinitionFile</span></span>
<span data-ttu-id="19735-118">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="19735-118">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19735-119">-Force</span><span class="sxs-lookup"><span data-stu-id="19735-119">-Force</span></span>
<span data-ttu-id="19735-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="19735-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="19735-121">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="19735-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="19735-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="19735-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19735-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19735-123">-ResourceGroupName</span></span>
<span data-ttu-id="19735-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="19735-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19735-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="19735-125">-Confirm</span></span>
<span data-ttu-id="19735-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19735-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19735-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19735-127">-WhatIf</span></span>
<span data-ttu-id="19735-128">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="19735-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19735-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19735-129">-DefaultProfile</span></span>
<span data-ttu-id="19735-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19735-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19735-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19735-131">CommonParameters</span></span>
<span data-ttu-id="19735-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19735-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19735-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19735-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19735-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19735-134">INPUTS</span></span>

### <span data-ttu-id="19735-135">System. String</span><span class="sxs-lookup"><span data-stu-id="19735-135">System.String</span></span>
<span data-ttu-id="19735-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="19735-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="19735-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19735-137">OUTPUTS</span></span>

### <span data-ttu-id="19735-138">System. String</span><span class="sxs-lookup"><span data-stu-id="19735-138">System.String</span></span>

## <span data-ttu-id="19735-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19735-139">NOTES</span></span>

## <span data-ttu-id="19735-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19735-140">RELATED LINKS</span></span>

