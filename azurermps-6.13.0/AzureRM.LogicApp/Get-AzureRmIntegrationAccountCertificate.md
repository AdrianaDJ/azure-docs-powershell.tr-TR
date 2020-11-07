---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 673c06cfd54f00a6d781d1415798e639875b7c46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764644"
---
# <span data-ttu-id="9af7e-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9af7e-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="9af7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9af7e-102">SYNOPSIS</span></span>
<span data-ttu-id="9af7e-103">Kaynak grubundan tümleştirme hesabı sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="9af7e-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9af7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9af7e-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9af7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9af7e-105">DESCRIPTION</span></span>
<span data-ttu-id="9af7e-106">**Get-AzureRmIntegrationAccountCertificate** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="9af7e-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="9af7e-107">Tümleştirme hesap adını, kaynak grubu adını ve sertifika adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="9af7e-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="9af7e-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="9af7e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9af7e-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="9af7e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9af7e-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="9af7e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9af7e-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="9af7e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9af7e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9af7e-112">EXAMPLES</span></span>

### <span data-ttu-id="9af7e-113">Örnek 1: Tümleştirme hesabı sertifikası alma</span><span class="sxs-lookup"><span data-stu-id="9af7e-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="9af7e-114">Bu komut, IntegrationAccountCertificate01 adlı tümleştirme hesabı sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="9af7e-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="9af7e-115">Örnek 2: Tümleştirme hesabı sertifikalarını tümleştirme hesap adıyla alma</span><span class="sxs-lookup"><span data-stu-id="9af7e-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="9af7e-116">Bu komut, IntegrationAccount31 adlı tümleştirme hesabı için tümleştirme hesabı sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="9af7e-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="9af7e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9af7e-117">PARAMETERS</span></span>

### <span data-ttu-id="9af7e-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9af7e-118">-CertificateName</span></span>
<span data-ttu-id="9af7e-119">Tümleştirme hesabı sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9af7e-119">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af7e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af7e-120">-DefaultProfile</span></span>
<span data-ttu-id="9af7e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9af7e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9af7e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9af7e-122">-Name</span></span>
<span data-ttu-id="9af7e-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9af7e-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af7e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af7e-124">-ResourceGroupName</span></span>
<span data-ttu-id="9af7e-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9af7e-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9af7e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af7e-126">CommonParameters</span></span>
<span data-ttu-id="9af7e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9af7e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af7e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af7e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af7e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9af7e-129">INPUTS</span></span>

### <span data-ttu-id="9af7e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9af7e-130">System.String</span></span>

## <span data-ttu-id="9af7e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9af7e-131">OUTPUTS</span></span>

### <span data-ttu-id="9af7e-132">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountcertificate</span><span class="sxs-lookup"><span data-stu-id="9af7e-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="9af7e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9af7e-133">NOTES</span></span>

## <span data-ttu-id="9af7e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9af7e-134">RELATED LINKS</span></span>

[<span data-ttu-id="9af7e-135">Yeni-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9af7e-135">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="9af7e-136">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9af7e-136">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="9af7e-137">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9af7e-137">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


