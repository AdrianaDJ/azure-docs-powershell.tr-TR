---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: a93eb93a02c0ba1f5654258da0405f723e69873d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761055"
---
# <span data-ttu-id="e3bd7-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="e3bd7-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="e3bd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bd7-103">Belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="e3bd7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3bd7-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3bd7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3bd7-105">DESCRIPTION</span></span>
<span data-ttu-id="e3bd7-106">**Remove-AzDataLakeStoreTrustedIdProvider** cmdlet 'ı belirtilen Data Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="e3bd7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3bd7-107">EXAMPLES</span></span>

### <span data-ttu-id="e3bd7-108">Örnek 1: güvenilir bir kimlik sağlayıcısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="e3bd7-109">"Benimsağlayıcı" sağlayıcısını "ContosoADL" hesabından kaldırır</span><span class="sxs-lookup"><span data-stu-id="e3bd7-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="e3bd7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3bd7-110">PARAMETERS</span></span>

### <span data-ttu-id="e3bd7-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="e3bd7-111">-Account</span></span>
<span data-ttu-id="e3bd7-112">Güvenilir kimlik sağlayıcısını kaldırmak için Data Lake Store hesabı</span><span class="sxs-lookup"><span data-stu-id="e3bd7-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="e3bd7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3bd7-113">-DefaultProfile</span></span>
<span data-ttu-id="e3bd7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e3bd7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3bd7-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3bd7-115">-Name</span></span>
<span data-ttu-id="e3bd7-116">Güvenilen kimlik sağlayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="e3bd7-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e3bd7-117">-PassThru</span></span>
<span data-ttu-id="e3bd7-118">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="e3bd7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3bd7-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3bd7-120">Güvenilen kimlik sağlayıcısını kaldırmak istediğiniz hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="e3bd7-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3bd7-121">-Confirm</span></span>
<span data-ttu-id="e3bd7-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3bd7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3bd7-123">-WhatIf</span></span>
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

### <span data-ttu-id="e3bd7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bd7-124">CommonParameters</span></span>
<span data-ttu-id="e3bd7-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3bd7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bd7-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3bd7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bd7-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3bd7-127">INPUTS</span></span>

### <span data-ttu-id="e3bd7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e3bd7-128">System.String</span></span>

### <span data-ttu-id="e3bd7-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e3bd7-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e3bd7-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3bd7-130">OUTPUTS</span></span>

### <span data-ttu-id="e3bd7-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3bd7-131">System.Boolean</span></span>

## <span data-ttu-id="e3bd7-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3bd7-132">NOTES</span></span>

## <span data-ttu-id="e3bd7-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3bd7-133">RELATED LINKS</span></span>
