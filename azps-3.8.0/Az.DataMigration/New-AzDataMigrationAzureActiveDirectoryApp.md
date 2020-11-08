---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098039"
---
# <span data-ttu-id="2844a-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="2844a-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="2844a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2844a-102">SYNOPSIS</span></span>
<span data-ttu-id="2844a-103">Yeni bir örnek oluştur DataMigration Azure ActiveDirectory uygulaması ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="2844a-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="2844a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2844a-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2844a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2844a-105">DESCRIPTION</span></span>
<span data-ttu-id="2844a-106">Yeni bir örnek oluştur DataMigration Azure ActiveDirectory uygulaması ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="2844a-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="2844a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2844a-107">EXAMPLES</span></span>

### <span data-ttu-id="2844a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2844a-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="2844a-109">ApplicationId: "AppID/hizmet asıl kimliği burada" AppKey: System. Security. SecureString Tenantıd: "Kiracı kimliği"</span><span class="sxs-lookup"><span data-stu-id="2844a-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="2844a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2844a-110">PARAMETERS</span></span>

### <span data-ttu-id="2844a-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="2844a-111">-AppKey</span></span>
<span data-ttu-id="2844a-112">Azure Active Directory anahtarı</span><span class="sxs-lookup"><span data-stu-id="2844a-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2844a-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2844a-113">-ApplicationId</span></span>
<span data-ttu-id="2844a-114">Azure Active Directory Uygulama kimliği</span><span class="sxs-lookup"><span data-stu-id="2844a-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2844a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2844a-115">-DefaultProfile</span></span>
<span data-ttu-id="2844a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2844a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2844a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2844a-117">CommonParameters</span></span>
<span data-ttu-id="2844a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2844a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2844a-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2844a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2844a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2844a-120">INPUTS</span></span>

### <span data-ttu-id="2844a-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2844a-121">None</span></span>

## <span data-ttu-id="2844a-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2844a-122">OUTPUTS</span></span>

### <span data-ttu-id="2844a-123">Microsoft. Azure. Commands. DataMigration. modeller. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="2844a-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="2844a-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2844a-124">NOTES</span></span>

## <span data-ttu-id="2844a-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2844a-125">RELATED LINKS</span></span>
