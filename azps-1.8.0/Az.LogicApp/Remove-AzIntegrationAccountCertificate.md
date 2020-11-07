---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 9e857d506b149c79d86ca52f2d3d7d3e3d598216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916000"
---
# <span data-ttu-id="c5714-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c5714-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="c5714-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5714-102">SYNOPSIS</span></span>
<span data-ttu-id="c5714-103">Kaynak grubundan bir tümleştirme hesabı sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c5714-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="c5714-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5714-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5714-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5714-105">DESCRIPTION</span></span>
<span data-ttu-id="c5714-106">**Remove-Azıntegrationaccountcertificate** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c5714-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="c5714-107">Tümleştirme hesap adını, kaynak grubu adını ve sertifika adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c5714-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="c5714-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="c5714-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c5714-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="c5714-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c5714-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="c5714-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c5714-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="c5714-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c5714-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5714-112">EXAMPLES</span></span>

### <span data-ttu-id="c5714-113">Örnek 1: Tümleştirme hesabı sertifikasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c5714-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="c5714-114">Bu komut, IntegrationAccount31 adlı tümleştirme hesabı sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c5714-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="c5714-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5714-115">PARAMETERS</span></span>

### <span data-ttu-id="c5714-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c5714-116">-CertificateName</span></span>
<span data-ttu-id="c5714-117">Tümleştirme hesabı sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5714-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="c5714-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5714-118">-DefaultProfile</span></span>
<span data-ttu-id="c5714-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c5714-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5714-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c5714-120">-Force</span></span>
<span data-ttu-id="c5714-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c5714-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5714-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5714-122">-Name</span></span>
<span data-ttu-id="c5714-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5714-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="c5714-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5714-124">-ResourceGroupName</span></span>
<span data-ttu-id="c5714-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5714-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c5714-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="c5714-126">-Confirm</span></span>
<span data-ttu-id="c5714-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c5714-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5714-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5714-128">-WhatIf</span></span>
<span data-ttu-id="c5714-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5714-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5714-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c5714-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5714-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5714-131">CommonParameters</span></span>
<span data-ttu-id="c5714-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5714-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5714-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5714-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5714-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5714-134">INPUTS</span></span>

### <span data-ttu-id="c5714-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c5714-135">System.String</span></span>

## <span data-ttu-id="c5714-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5714-136">OUTPUTS</span></span>

### <span data-ttu-id="c5714-137">System. void</span><span class="sxs-lookup"><span data-stu-id="c5714-137">System.Void</span></span>

## <span data-ttu-id="c5714-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5714-138">NOTES</span></span>

## <span data-ttu-id="c5714-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5714-139">RELATED LINKS</span></span>

[<span data-ttu-id="c5714-140">Get-Azıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="c5714-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="c5714-141">Yeni-az</span><span class="sxs-lookup"><span data-stu-id="c5714-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="c5714-142">Set-Azıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="c5714-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


