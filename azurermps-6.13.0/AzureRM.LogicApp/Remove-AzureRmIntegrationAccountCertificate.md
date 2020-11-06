---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 04aa8bfff795bc98b4458acb18f23535ce8bb024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590211"
---
# <span data-ttu-id="93302-101">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="93302-101">Remove-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="93302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93302-102">SYNOPSIS</span></span>
<span data-ttu-id="93302-103">Kaynak grubundan bir tümleştirme hesabı sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93302-103">Removes an integration account certificate from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93302-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93302-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String>
 -CertificateName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93302-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="93302-105">DESCRIPTION</span></span>
<span data-ttu-id="93302-106">**Remove-AzureRmIntegrationAccountCertificate** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93302-106">The **Remove-AzureRmIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="93302-107">Tümleştirme hesap adını, kaynak grubu adını ve sertifika adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="93302-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="93302-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="93302-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="93302-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="93302-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="93302-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="93302-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="93302-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="93302-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="93302-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93302-112">EXAMPLES</span></span>

### <span data-ttu-id="93302-113">Örnek 1: Tümleştirme hesabı sertifikasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="93302-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="93302-114">Bu komut, IntegrationAccount31 adlı tümleştirme hesabı sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93302-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="93302-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93302-115">PARAMETERS</span></span>

### <span data-ttu-id="93302-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="93302-116">-CertificateName</span></span>
<span data-ttu-id="93302-117">Tümleştirme hesabı sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93302-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="93302-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93302-118">-DefaultProfile</span></span>
<span data-ttu-id="93302-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="93302-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93302-120">-Force</span><span class="sxs-lookup"><span data-stu-id="93302-120">-Force</span></span>
<span data-ttu-id="93302-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="93302-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93302-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="93302-122">-Name</span></span>
<span data-ttu-id="93302-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93302-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93302-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93302-124">-ResourceGroupName</span></span>
<span data-ttu-id="93302-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93302-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="93302-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="93302-126">-Confirm</span></span>
<span data-ttu-id="93302-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93302-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93302-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93302-128">-WhatIf</span></span>
<span data-ttu-id="93302-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93302-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93302-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="93302-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93302-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93302-131">CommonParameters</span></span>
<span data-ttu-id="93302-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93302-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93302-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93302-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93302-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93302-134">INPUTS</span></span>

### <span data-ttu-id="93302-135">System. String</span><span class="sxs-lookup"><span data-stu-id="93302-135">System.String</span></span>

## <span data-ttu-id="93302-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93302-136">OUTPUTS</span></span>

### <span data-ttu-id="93302-137">System. void</span><span class="sxs-lookup"><span data-stu-id="93302-137">System.Void</span></span>

## <span data-ttu-id="93302-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93302-138">NOTES</span></span>

## <span data-ttu-id="93302-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93302-139">RELATED LINKS</span></span>

[<span data-ttu-id="93302-140">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="93302-140">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="93302-141">Yeni-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="93302-141">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="93302-142">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="93302-142">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


