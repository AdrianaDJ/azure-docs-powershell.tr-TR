---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: f281192e22cd8acdf85e389d82ef7146590be158
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572789"
---
# <span data-ttu-id="937d1-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="937d1-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="937d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="937d1-102">SYNOPSIS</span></span>
<span data-ttu-id="937d1-103">Belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="937d1-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="937d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="937d1-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="937d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="937d1-105">DESCRIPTION</span></span>
<span data-ttu-id="937d1-106">**Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet 'ı belirtilen Data Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="937d1-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="937d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="937d1-107">EXAMPLES</span></span>

### <span data-ttu-id="937d1-108">Örnek 1: güvenilir bir kimlik sağlayıcısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="937d1-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="937d1-109">"Benimsağlayıcı" sağlayıcısını "ContosoADL" hesabından kaldırır</span><span class="sxs-lookup"><span data-stu-id="937d1-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="937d1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="937d1-110">PARAMETERS</span></span>

### <span data-ttu-id="937d1-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="937d1-111">-Account</span></span>
<span data-ttu-id="937d1-112">Güvenilir kimlik sağlayıcısını kaldırmak için Data Lake Store hesabı</span><span class="sxs-lookup"><span data-stu-id="937d1-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="937d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937d1-113">-DefaultProfile</span></span>
<span data-ttu-id="937d1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="937d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="937d1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="937d1-115">-Name</span></span>
<span data-ttu-id="937d1-116">Güvenilen kimlik sağlayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="937d1-116">The name of the trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="937d1-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="937d1-117">-PassThru</span></span>
<span data-ttu-id="937d1-118">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="937d1-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="937d1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="937d1-119">-ResourceGroupName</span></span>
<span data-ttu-id="937d1-120">Güvenilen kimlik sağlayıcısını kaldırmak istediğiniz hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="937d1-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="937d1-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="937d1-121">-Confirm</span></span>
<span data-ttu-id="937d1-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="937d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="937d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="937d1-123">-WhatIf</span></span>
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

### <span data-ttu-id="937d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937d1-124">CommonParameters</span></span>
<span data-ttu-id="937d1-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="937d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937d1-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="937d1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937d1-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="937d1-127">INPUTS</span></span>

### <span data-ttu-id="937d1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="937d1-128">System.String</span></span>

### <span data-ttu-id="937d1-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="937d1-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="937d1-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="937d1-130">OUTPUTS</span></span>

### <span data-ttu-id="937d1-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="937d1-131">System.Boolean</span></span>

## <span data-ttu-id="937d1-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="937d1-132">NOTES</span></span>

## <span data-ttu-id="937d1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="937d1-133">RELATED LINKS</span></span>
