---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 5b8da61caf8e3a89572f2054aea101a1ad8b70c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095915"
---
# <span data-ttu-id="3dbbf-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3dbbf-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="3dbbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="3dbbf-103">Tümleştirme hesabı sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="3dbbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3dbbf-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3dbbf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3dbbf-105">DESCRIPTION</span></span>
<span data-ttu-id="3dbbf-106">**Set-Azıntegrationaccountcertificate** cmdlet 'i bir tümleştirme hesabı sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="3dbbf-107">Bu cmdlet, tümleştirme hesabı sertifikasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="3dbbf-108">Tümleştirme hesap adını, kaynak grubu adını ve sertifika adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="3dbbf-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3dbbf-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3dbbf-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3dbbf-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3dbbf-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3dbbf-113">EXAMPLES</span></span>

### <span data-ttu-id="3dbbf-114">Örnek 1: Tümleştirme hesabı sertifikasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="3dbbf-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="3dbbf-115">Bu komut, belirtilen kaynak grubundaki tümleştirme hesabı sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="3dbbf-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3dbbf-116">PARAMETERS</span></span>

### <span data-ttu-id="3dbbf-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="3dbbf-117">-CertificateName</span></span>
<span data-ttu-id="3dbbf-118">Tümleştirme hesabı sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="3dbbf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dbbf-119">-DefaultProfile</span></span>
<span data-ttu-id="3dbbf-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3dbbf-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3dbbf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3dbbf-121">-Force</span></span>
<span data-ttu-id="3dbbf-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3dbbf-123">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="3dbbf-123">-KeyName</span></span>
<span data-ttu-id="3dbbf-124">Anahtar kasasındaki sertifika anahtarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-124">Specifies the name of a certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbbf-125">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="3dbbf-125">-KeyVaultId</span></span>
<span data-ttu-id="3dbbf-126">Bir anahtar kasa KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-126">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbbf-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="3dbbf-127">-KeyVersion</span></span>
<span data-ttu-id="3dbbf-128">Anahtar kasasındaki sertifika anahtarının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbbf-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3dbbf-129">-Metadata</span></span>
<span data-ttu-id="3dbbf-130">Sertifikanın meta veri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-130">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbbf-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="3dbbf-131">-Name</span></span>
<span data-ttu-id="3dbbf-132">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-132">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbbf-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3dbbf-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="3dbbf-134">Ortak sertifika (. cer) dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbbf-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dbbf-135">-ResourceGroupName</span></span>
<span data-ttu-id="3dbbf-136">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3dbbf-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="3dbbf-137">-Confirm</span></span>
<span data-ttu-id="3dbbf-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dbbf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dbbf-139">-WhatIf</span></span>
<span data-ttu-id="3dbbf-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dbbf-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dbbf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dbbf-142">CommonParameters</span></span>
<span data-ttu-id="3dbbf-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3dbbf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dbbf-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dbbf-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dbbf-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3dbbf-145">INPUTS</span></span>

### <span data-ttu-id="3dbbf-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3dbbf-146">System.String</span></span>

## <span data-ttu-id="3dbbf-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3dbbf-147">OUTPUTS</span></span>

### <span data-ttu-id="3dbbf-148">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="3dbbf-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="3dbbf-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3dbbf-149">NOTES</span></span>

## <span data-ttu-id="3dbbf-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3dbbf-150">RELATED LINKS</span></span>

[<span data-ttu-id="3dbbf-151">Get-Azıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="3dbbf-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="3dbbf-152">Yeni-az</span><span class="sxs-lookup"><span data-stu-id="3dbbf-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="3dbbf-153">Remove-Azıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="3dbbf-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

