---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 651ce1141e9a925d5571f8b70d8eecedb4a1e66d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274478"
---
# <span data-ttu-id="60c34-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="60c34-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="60c34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60c34-102">SYNOPSIS</span></span>
<span data-ttu-id="60c34-103">Tümleştirme hesabı sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60c34-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="60c34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60c34-104">SYNTAX</span></span>

### <span data-ttu-id="60c34-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="60c34-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c34-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="60c34-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c34-107">De</span><span class="sxs-lookup"><span data-stu-id="60c34-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60c34-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60c34-108">DESCRIPTION</span></span>
<span data-ttu-id="60c34-109">**New-Azıntegrationaccountcertificate** cmdlet 'i bir tümleştirme hesabı sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60c34-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="60c34-110">Bu cmdlet, tümleştirme hesabı sertifikasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="60c34-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="60c34-111">Tümleştirme hesap adını, kaynak grubu adını, sertifika adını, anahtar adını, anahtar sürümü ve Anahtar Kasası KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="60c34-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="60c34-112">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="60c34-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="60c34-113">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="60c34-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="60c34-114">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="60c34-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="60c34-115">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="60c34-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="60c34-116">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="60c34-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="60c34-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60c34-117">EXAMPLES</span></span>

### <span data-ttu-id="60c34-118">Örnek 1: Tümleştirme hesabı sertifikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="60c34-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="60c34-119">Bu komut, belirtilen kaynak grubunda tümleştirme hesabı sertifikasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60c34-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="60c34-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60c34-120">PARAMETERS</span></span>

### <span data-ttu-id="60c34-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="60c34-121">-CertificateName</span></span>
<span data-ttu-id="60c34-122">Tümleştirme hesabı sertifikası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="60c34-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="60c34-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c34-123">-DefaultProfile</span></span>
<span data-ttu-id="60c34-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="60c34-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60c34-125">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="60c34-125">-KeyName</span></span>
<span data-ttu-id="60c34-126">Anahtar kasasındaki sertifika anahtarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60c34-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c34-127">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="60c34-127">-KeyVaultId</span></span>
<span data-ttu-id="60c34-128">Bir anahtar kasa KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="60c34-128">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c34-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="60c34-129">-KeyVersion</span></span>
<span data-ttu-id="60c34-130">Anahtar kasasındaki sertifika anahtarının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="60c34-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c34-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="60c34-131">-Metadata</span></span>
<span data-ttu-id="60c34-132">Sertifikanın meta veri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="60c34-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="60c34-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="60c34-133">-Name</span></span>
<span data-ttu-id="60c34-134">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60c34-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="60c34-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="60c34-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="60c34-136">Ortak sertifika (. cer) dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="60c34-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c34-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c34-137">-ResourceGroupName</span></span>
<span data-ttu-id="60c34-138">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60c34-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="60c34-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="60c34-139">-Confirm</span></span>
<span data-ttu-id="60c34-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="60c34-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60c34-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60c34-141">-WhatIf</span></span>
<span data-ttu-id="60c34-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="60c34-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60c34-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="60c34-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60c34-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c34-144">CommonParameters</span></span>
<span data-ttu-id="60c34-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60c34-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c34-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c34-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c34-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60c34-147">INPUTS</span></span>

### <span data-ttu-id="60c34-148">System. String</span><span class="sxs-lookup"><span data-stu-id="60c34-148">System.String</span></span>

## <span data-ttu-id="60c34-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60c34-149">OUTPUTS</span></span>

### <span data-ttu-id="60c34-150">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="60c34-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="60c34-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60c34-151">NOTES</span></span>

## <span data-ttu-id="60c34-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60c34-152">RELATED LINKS</span></span>

[<span data-ttu-id="60c34-153">Get-Azıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="60c34-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="60c34-154">Remove-Azıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="60c34-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="60c34-155">Set-Azıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="60c34-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


