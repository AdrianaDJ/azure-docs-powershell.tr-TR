---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: feb885ca6f08a7396fd88db73d48172dc002f055
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593093"
---
# <span data-ttu-id="8ebf8-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8ebf8-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="8ebf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ebf8-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebf8-103">Tümleştirme hesabı sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ebf8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ebf8-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ebf8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ebf8-105">DESCRIPTION</span></span>
<span data-ttu-id="8ebf8-106">**Set-AzureRmIntegrationAccountCertificate** cmdlet 'i bir tümleştirme hesabı sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="8ebf8-107">Bu cmdlet, tümleştirme hesabı sertifikasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="8ebf8-108">Tümleştirme hesap adını, kaynak grubu adını ve sertifika adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-108">Specifying the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="8ebf8-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8ebf8-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8ebf8-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8ebf8-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8ebf8-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ebf8-113">EXAMPLES</span></span>

### <span data-ttu-id="8ebf8-114">Örnek 1: Tümleştirme hesabı sertifikasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="8ebf8-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="8ebf8-115">Bu komut, belirtilen kaynak grubundaki tümleştirme hesabı sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="8ebf8-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ebf8-116">PARAMETERS</span></span>

### <span data-ttu-id="8ebf8-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="8ebf8-117">-CertificateName</span></span>
<span data-ttu-id="8ebf8-118">Tümleştirme hesabı sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="8ebf8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8ebf8-119">-Force</span></span>
<span data-ttu-id="8ebf8-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ebf8-121">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="8ebf8-121">-KeyName</span></span>
<span data-ttu-id="8ebf8-122">Anahtar kasasındaki sertifika anahtarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-122">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="8ebf8-123">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="8ebf8-123">-KeyVaultId</span></span>
<span data-ttu-id="8ebf8-124">Bir anahtar kasa KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-124">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="8ebf8-125">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="8ebf8-125">-KeyVersion</span></span>
<span data-ttu-id="8ebf8-126">Anahtar kasasındaki sertifika anahtarının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-126">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="8ebf8-127">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8ebf8-127">-Metadata</span></span>
<span data-ttu-id="8ebf8-128">Sertifikanın meta veri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-128">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="8ebf8-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ebf8-129">-Name</span></span>
<span data-ttu-id="8ebf8-130">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-130">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="8ebf8-131">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="8ebf8-131">-PublicCertificateFilePath</span></span>
<span data-ttu-id="8ebf8-132">Ortak sertifika (. cer) dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-132">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="8ebf8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ebf8-133">-ResourceGroupName</span></span>
<span data-ttu-id="8ebf8-134">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8ebf8-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ebf8-135">-Confirm</span></span>
<span data-ttu-id="8ebf8-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ebf8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ebf8-137">-WhatIf</span></span>
<span data-ttu-id="8ebf8-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ebf8-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ebf8-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebf8-140">-DefaultProfile</span></span>
<span data-ttu-id="8ebf8-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ebf8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebf8-142">CommonParameters</span></span>
<span data-ttu-id="8ebf8-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ebf8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebf8-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ebf8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebf8-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ebf8-145">INPUTS</span></span>

## <span data-ttu-id="8ebf8-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ebf8-146">OUTPUTS</span></span>

### <span data-ttu-id="8ebf8-147">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="8ebf8-147">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="8ebf8-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ebf8-148">NOTES</span></span>

## <span data-ttu-id="8ebf8-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ebf8-149">RELATED LINKS</span></span>

[<span data-ttu-id="8ebf8-150">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8ebf8-150">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="8ebf8-151">Yeni-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8ebf8-151">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="8ebf8-152">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8ebf8-152">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)


