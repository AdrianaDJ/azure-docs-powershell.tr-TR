---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 907bf32bfa38aa29fc75074e5037211615a16af7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938324"
---
# <span data-ttu-id="b2979-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="b2979-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="b2979-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2979-102">SYNOPSIS</span></span>
<span data-ttu-id="b2979-103">Bağlı hizmette kimlik bilgilerini belirtilen tümleştirme çalışma zamanına göre şifrele.</span><span class="sxs-lookup"><span data-stu-id="b2979-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="b2979-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2979-104">SYNTAX</span></span>

### <span data-ttu-id="b2979-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2979-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2979-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b2979-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2979-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2979-107">DESCRIPTION</span></span>
<span data-ttu-id="b2979-108">New-AzDataFactoryV2LinkedServiceEncryptCredential cmdlet 'i, bağlantılı hizmette belirtilen tümleştirme çalışma zamanına sahip kimlik bilgilerini şifreler.</span><span class="sxs-lookup"><span data-stu-id="b2979-108">The New-AzDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="b2979-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2979-109">EXAMPLES</span></span>

### <span data-ttu-id="b2979-110">Örnek 1: bağlantılı hizmette kimlik bilgilerini şifreleme</span><span class="sxs-lookup"><span data-stu-id="b2979-110">Example 1: Encrypt credentials in a linked service</span></span>
```
PS C:\> New-AzDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="b2979-111">Bu komut, D:\sql.jsdosyadaki kimlik bilgilerini Mycır adlı tümleştirme çalışma zamanıyla şifreler.</span><span class="sxs-lookup"><span data-stu-id="b2979-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="b2979-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2979-112">PARAMETERS</span></span>

### <span data-ttu-id="b2979-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b2979-113">-DataFactory</span></span>
<span data-ttu-id="b2979-114">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b2979-114">The data factory object.</span></span>

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

### <span data-ttu-id="b2979-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b2979-115">-DataFactoryName</span></span>
<span data-ttu-id="b2979-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="b2979-116">The data factory name.</span></span>

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

### <span data-ttu-id="b2979-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2979-117">-DefaultProfile</span></span>
<span data-ttu-id="b2979-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2979-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2979-119">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="b2979-119">-DefinitionFile</span></span>
<span data-ttu-id="b2979-120">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="b2979-120">The JSON file path.</span></span>

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

### <span data-ttu-id="b2979-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b2979-121">-Force</span></span>
<span data-ttu-id="b2979-122">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="b2979-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b2979-123">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="b2979-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b2979-124">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="b2979-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="b2979-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2979-125">-ResourceGroupName</span></span>
<span data-ttu-id="b2979-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b2979-126">The resource group name.</span></span>

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

### <span data-ttu-id="b2979-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b2979-127">-Confirm</span></span>
<span data-ttu-id="b2979-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b2979-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2979-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2979-129">-WhatIf</span></span>
<span data-ttu-id="b2979-130">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="b2979-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b2979-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2979-131">CommonParameters</span></span>
<span data-ttu-id="b2979-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2979-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2979-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2979-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2979-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2979-134">INPUTS</span></span>

### <span data-ttu-id="b2979-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b2979-135">System.String</span></span>

### <span data-ttu-id="b2979-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="b2979-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b2979-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2979-137">OUTPUTS</span></span>

### <span data-ttu-id="b2979-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b2979-138">System.String</span></span>

## <span data-ttu-id="b2979-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2979-139">NOTES</span></span>

## <span data-ttu-id="b2979-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2979-140">RELATED LINKS</span></span>